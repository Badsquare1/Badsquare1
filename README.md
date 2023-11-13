- 👋 Hi, I’m @Badsquare1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Badsquare1/Badsquare1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Array = list()
Pilha = list()
Fila = list()
Árvore = list()
Grafo = list()

Array_cont = 0
Pilha_cont = 0
Fila_cont = 0
Árvore_cont = 0
Grafo_cont = 0

all_together = [Array, Pilha, Fila, Árvore, Grafo, Array_cont, Pilha_cont, Fila_cont, Árvore_cont, Grafo_cont]
#==================================================================================
print("Olá! Meu nome é Edu, vou te ajudar a escolher a estrutura para armazenamento de dados\nmais eficiente para o tipo de projeto que você está executando. Depois que tivermos escolhido\na estrutura ideal, te ajudarei implementá-la, ok!?")

Pergunta_1 = int(input("Se x for essencial pra você, digite 1. Se não for, digite 2. Caso seja irrelevante, digite 3.\n"))

def pergunta1(Pergunta_1):
    if Pergunta_1 == 1:
        Array.append('Essa parte é muito usada para pipipi popopo')
        Array_cont =+ 1
        print(Array)
    elif Pergunta_1 == 2:
        Pilha.append('se a parte tal ser feita de tal jeito, está certo')
        Pilha_cont =+ 1
        print(Pilha)
    elif Pergunta_1 == 3:
        pass       
    else:
        Pergunta_1 = int(input("Insira um valor válido.\n"))
        pergunta1(Pergunta_1)
     
pergunta1(Pergunta_1)
'''Pergunta_1 = int(input("Se x for essencial pra você, digite 1. Se não for, digite 2. Caso seja irrelevante, digite 3.\n"))
if Pergunta_1 == 1:
     Array.append('Essa parte é muito usada para pipipi popopo')
     Array_cont += 1
     print(Array)
elif Pergunta_1 == 2:
     Pilha.append('se a parte tal ser feita de tal jeito, está certo')
     Pilha_cont =+ 1
     print(Pilha)
elif Pergunta_1 == 3:
     pass       
else:
    while Pergunta_1 != 1 or 2 or 3:
        Pergunta_1 = int(input("Se x for essencial pra você, digite 1. Se não for, digite 2. Caso seja irrelevante, digite 3.\nEnsira um número válido.\n"))'''
        
'''if Pergunta_1 == 1:
     Array.append('Essa parte é muito usada para pipipi popopo')
     Array_cont += 1
     print(Array)
elif Pergunta_1 == 2:
     Pilha.append('se a parte tal ser feita de tal jeito, está certo')
     Pilha_cont =+ 1
     print(Pilha)    
elif Pergunta_1 == 3:
     pass    '''  
    
    

'''total = max(Array_cont, Pilha_cont, Fila_cont, Árvore_cont, Grafo_cont) #NÃO PODE HAVER POSSIBILIDADE DE EMPATAR)
print(total)'''
