-----> Edu, Assitente Virtual 

-----> Edu é um assistente virtual que foi criado pelo Marcelo Velozo (matrícula: 222026232) e pela Maira Silva (matrícula: 222026214). O propósito dele é auxiliar pessoas a encontrar a estrutura de dados ideal para os seus projetos, isso é feito através de algumas perguntas. Após o final do questionário, o Edu te ajuda a implementar o código! 

-----> Utilizamos alguns Arrays simples para implementar esse projeto. 

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

print('Olá! Meu nome é Edu, vou te ajudar a escolher a estrutura para armazenamento de dados\nmais eficiente para o tipo de projeto que voce esta executando. Depois que tivermos escolhido\na estrutura ideal, te ajudarei implrmenta-la, ok!?\n')

print('Para começar, vou te fazer algumas perguntas, responda conforme as orientações de cada pergunta :)\n')
Pergunta_1 = int(input('Os dados que forem inseridos terão relações entre si, ou serão apenas dados independentes?\n\033[1;35mDigite 1 para dados interligados e 2 para dados independentes.\033[m\n\n'))
condic_1 = False

def pergunta1(Pergunta_1, condic_1):
    while condic_1 != True:
        if 3 > Pergunta_1 > 0 :
            condic_1 = True
            return(Pergunta_1)
        else:
            pass
            Pergunta_1 = int(input('\n\033[1;35mInsira uma opção válida!\033[m\n\n'))

Pergunta_1 = pergunta1(Pergunta_1, condic_1)
print(Pergunta_1)



if Pergunta_1 == 1:
    Array_cont += 1
    Array_frase.append('Essa parte é muito usada pra pipi popopo')
elif Pergunta_1 == 2:
    Pilha_cont += 1
    Pilha_frase.append('Se a parte tal ser feita de tal jeito, esta certo')


print(Array_frase)

dic = {'Array': Array_cont, 'Pilha':Pilha_cont, 'Fila': Fila_cont, 'Arvore':Arvore_cont, 'Grafo':Grafo_cont}
total = max(dic, key = dic.get)
print(total)



if total == 'Array':
    print('Resultado: a lista é a estrutura de dados ideal para o seu projeto!')
    print(Array_frase)
elif total == 'Pilha':
    print('Resultado: a pilha é a estrutura de dados ideal para o seu projeto!')
    print(Pilha_frase)
elif total == 'Fila':
    print('Resultado: a fila é a estrutura de dados ideal para o seu projeto!')
    print(Fila_frase)
elif total == 'Arvore':
    print('Resultado: a árvore é a estrutura de dados ideal para o seu projeto!')
    print(Arvore_frase)
elif total == 'Grafo':
    print('Resultado: o grafo é a estrutura de dados ideal para o seu projeto!')
    print(Grafo_frase)
