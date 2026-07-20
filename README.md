# Variveis-String ( armazenam cadeias de caracteres, nome e textos em geral ) para fazer a separeção de uma String usamos " utilizada também para armazenar sequência de caracteres, utilizada para exibir mensagens e gerar outros arquivos. Para opter um tamanho de uma String usamos a função len.
len("A")
1
len("AB")
2
len("")
0
len("O rato roeu a roupa")
18
# teste com strings
a="ABCDEF"
a[0]
'A'
a[1]
'B'
a[5]
'F'
len(a)
6
a[6]
Traceback (most recent call last):
  File "<pyshell#5>", line 1, in <module>
    a[6]
IndexError: string index out of range
# O peração com strings, varíaveis de tipo strings suportam operações, fatiamento, comcatenação e composição. ( fatiamento capacidade de utilizar parte da strings), ( Concatenação, poder juntar duas ou mais strings em uma nova string maior) ( Composição utilizada em mensagens que enviamos à tela).
# concatenação, para somados as strings usamos o sinal de + e para a repetição o sinal de * 
S= "ABC"
S+ "C"
'ABCC'
S+ "D" * 4
'ABCDDDD'
"X" + "-" * 10 + "X"
'X----------X'
S+ "X4= "+S*4
'ABCX4= ABCABCABCABC'
# ESSA FORMA DE CONCATENAÇÃO SÓ PODE SER USADA COM STRINGS
nome="Matheus"
idade="29"
nome+idade
'Matheus29'
# composição
%d # números inteiros
%s # Strings
%f # números decimais
idade=29
"[%d]" % idade
'[29]'
"[%03d]" % idade
'[029]'
"[%3d]" % idade
'[ 29]'
"[%-3d]" % idade
'[29 ]'
"%5f"%7
'7.000000'
"%5.2"%7
Traceback (most recent call last):
  File "<pyshell#9>", line 1, in <module>
    "%5.2"%7
ValueError: incomplete format
"%5.2f"%7
' 7.00'
"%10.5f"%7
'   7.00000'
nome= "Matheus"
idade=29
grane=51.34 #erro ao não prestar atenção na digitação
"%s tem %d anos e R$%f no bolso." % (nome,idade,grana)
Traceback (most recent call last): # por falta de atenção ocorreu um erro no codigo.
  File "<pyshell#15>", line 1, in <module>
    "%s tem %d anos e R$%f no bolso." % (nome,idade,grana)
NameError: name 'grana' is not defined. Did you mean: 'grane'?
nome="Matheus" # novo teste sem erro.
idade=29
grana=51.35
"%s tem %d anos e R$%f no bolso."%(nome,idade,grana)
'Matheus tem 29 anos e R$51.350000 no bolso.'
"%12s tem %3d anos e R$%5.2f no bolso."%(nome,idade,grana)
'     Matheus tem  29 anos e R$51.35 no bolso.'
"%12s tem %03d anos e R$%5.2f no bolso."%(nome,idade,grana)
'     Matheus tem 029 anos e R$51.35 no bolso.'
"%-12s tem %-3d anos e R$%-5.2f no bolso."%(nome,idade,grana)
'Matheus      tem 29  anos e R$51.35 no bolso.'
# usando o método 'format' mais simples do anterior 
nome=Rodrigo # erro de digitação
Traceback (most recent call last): # causou erro no codigo
  File "<pyshell#23>", line 1, in <module>
    nome=Rodrigo # mesmo erro na digitação
NameError: name 'Rodrigo' is not defined # erro no codigo
nome"Rodrigo"
SyntaxError: invalid syntax
nome="Rodrigo"
idade=32
grana=51.34
"{} tem {} anos e R${} no bolso.".format(nome,idade,grana)
'Rodrigo tem 32 anos e R$51.34 no bolso.'
nome=Rodrigo
Traceback (most recent call last):
  File "<pyshell#23>", line 1, in <module>
    nome=Rodrigo
NameError: name 'Rodrigo' is not defined
nome"Rodrigo"
SyntaxError: invalid syntax
nome="Rodrigo"
idade=32
grana=51.34
"{} tem {} anos e R${} no bolso.".format(nome,idade,grana)
'Rodrigo tem 32 anos e R$51.34 no bolso.'
"{:12} tem {:3} anos e R${:5.2f} no bolso.".format(nome,idade,grana)
'Rodrigo      tem  32 anos e R$51.34 no bolso.'
"[:12} tem {:03} anos e R${5.2f} no bolso.".format(nome.idade,grana) # erro no codigo
Traceback (most recent call last):
  File "<pyshell#30>", line 1, in <module>
    "[:12} tem {:03} anos e R${5.2f} no bolso.".format(nome.idade,grana)
AttributeError: 'str' object has no attribute 'idade'
"{:12} tem {:03} anos e R${:5.2f} no bolso.".format(nome,idade,grana)
'Rodrigo      tem 032 anos e R$51.34 no bolso.'
"{:<12s} tem {:<3} anos e R${:5.2f} no bolso.".format(nome,idade,grana)
'Rodrigo      tem 32  anos e R$51.34 no bolso.'
# fatiamento de strings, permite dividir uma strings em pedaços menores o fatiamento funciona usando : 
s="ABCDEFGHI"
s[0:2]
'AB'
s[1:2]
'B'
s[2:4]
'CD'
s[0:5]
'ABCDE'
s[1:8]
'BCDEFGH'
# omitir usando o :
s="ABCDEFGHI"
s[:2]
'AB'
s[:1]
'A'
s[1:]
'BCDEFGHI'
s[:]
'ABCDEFGHI'
s[3:]
'DEFGHI'
# posso utilizar valores negativos para indicar posições ( -1 é o último caractere, -2 o penultimo)
s="ABCDEFGHI"
s[:2]
'AB'
s[:1]
'A'
s[1:]
'BCDEFGHI'
s[:]
'ABCDEFGHI'
s[3:]
'DEFGHI'
s="ABCDEFGHI"
s[0:-2]
'ABCDEFG'
s[-1:]
'I'
s[-2:3]
''
s[-5:-7]
''
s[-5:7]
'EFG'
s[-2:-1]
'H'
# para inverter usando o recurso simples da fatia usando um terceiro parâmetro usando -1 invertendo a string
s="ABCDEFGHI"
s[::-1]
'IHGFEDCBA'
