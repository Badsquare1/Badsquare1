-----> Edu, Assitente Virtual 

-----> Edu é um assistente virtual que foi criado pelo Marcelo Velozo (matrícula: 222026232) e pela Maira Silva (matrícula: 222026214). O propósito dele é auxiliar pessoas a encontrar a estrutura de dados ideal para os seus projetos, isso é feito através de algumas perguntas. Após o final do questionário, o Edu te ajuda a implementar o código! 

-----> Utilizamos alguns Arrays simples para implementar esse projeto. 

from tkinter import *

Array = list()
Pilha = list()
Fila = list()
Arvore = list()
Grafo = list()

#==================================================================================

Array_cont = 0
Pilha_cont = 0
Fila_cont = 0
Arvore_cont = 0
Grafo_cont = 0

print('Olá! Meu nome é Edu, vou te ajudar a escolher a estrutura para armazenamento de dados\nmais eficiente para o tipo de projeto que voce esta executando. Depois que tivermos escolhido\na estrutura ideal, te ajudarei implrmenta-la, ok!?\n')

print('Para começar, vou te fazer algumas perguntas, responda conforme as orientações de cada pergunta :)\n')

Pergunta_1 = int(input('Os dados que forem inseridos terão relações entre si, ou serão apenas dados independentes?\n\033[1;35mDigite 1 para dados interligados e 2 para dados independentes.\033[m\n\n'))
condic_1 = False

def perguntas(Pergunta_1, condic_1):
    while condic_1 != True:
        if 4 > Pergunta_1 > 0 :
            condic_1 = True
            return(Pergunta_1)
        else:
            Pergunta_1 = int(input('Inserir valor valido!\n'))

Pergunta_1 = int(input('\n\033[1;31mO projeto tera uma quantidade pré-definida de dados?\n\033[m\n'))
condic_1 = 0
perguntas(Pergunta_1, condic_1)
if Pergunta_1 == 1:
    Array_cont += 2

Pergunta_2 = int(input('\n\033[1;31mOs dados inseridos teram relação entre si?\n\033[m\n'))
condic_2 = 0
perguntas(Pergunta_2, condic_2)
if Pergunta_2 == 1:
    Grafo_cont += 1
    Arvore_cont += 1

Pergunta_3 = int(input('\n\033[1;31mHaverá ligação direta e recíproca entre 2 ou mais elementos (formação de rede)?\n\033[m\n'))
condic_3 = 0
perguntas(Pergunta_3, condic_3)
if Pergunta_3 == 1:
    Grafo_cont += 2
    
    
Pergunta_4 = int(input('\n\033[1;31mA inserção e remoção de itens devem seguir um principio, como LIFO(Last in, first out) ou FIFO (First in, first out)?\n\033[m\n'))
condic_4 = 0
perguntas(Pergunta_4, condic_4)
if Pergunta_4 == 1:
    Pilha_cont += 1
    Fila_cont += 1
    
Pergunta_5 = int(input('\n\033[1;31mDeseja que o código seja implementado de forma recursiva?\n\033[m\n'))
condic_5 = 0
perguntas(Pergunta_5, condic_5)
if Pergunta_5 == 1:
    Pilha_cont += 2
    
Pergunta_6 = int(input('\n\033[1;31mDeseja que a estrutura seja organizada de forma linear?\n\033[m\n'))
condic_6 = 0
perguntas(Pergunta_6, condic_6)
if Pergunta_6 == 1:
    Array_cont += 1
    Pilha_cont += 1
    Fila_cont += 1
elif Pergunta_6 == 2:
    Grafo_cont += 1
    Arvore_cont += 1

Pergunta_7 = int(input('\n\033[1;31mDeseja que o acesso aos elementos seja em tempo constante?\n\033[m\n'))
condic_7 = 0
perguntas(Pergunta_7, condic_7)
if Pergunta_7 == 1:
    Array_cont += 1
    
Pergunta_8 = int(input('\n\033[1;31mVocê gostaria que estratutura tivesse mais de uma opção de implementação?\n\033[m\n'))
condic_8 = 0
perguntas(Pergunta_8, condic_8)
if Pergunta_8 == 1:
    Fila_cont += 2
    Arvore_cont += 1
    
Pergunta_9 =int(input('\n\033[1;31mHaverá hierarquia entre as informações? (ex.: contatos ou dependentes relacionados a um consumidor específico em um banco de dados)\n\033[m\n'))
condic_9 = 0
perguntas(Pergunta_9, condic_9)
if Pergunta_9 == 1:
    Arvore_cont += 2
    





dic = {'Array': Array_cont, 'Pilha':Pilha_cont, 'Fila': Fila_cont, 'Arvore':Arvore_cont, 'Grafo':Grafo_cont}
total = max(dic, key = dic.get)
print(total)

#=================================================================================================================================
#funções a serem chamadas dependendo do resultado

def caso_lista():
    
    print('Para emplementar uma lista precisamos primeiro saber especificamente qual é o melhor tipo pra sua situação!\n\nTemos 3 opções principais: \n\033[1;97;44mo Array, o Array Dinâmico e a Lista Encadeada.\033[m')
    print('\nCada um tem as suas especificidades, então vou te explicar um pouco mais sobre cada opção, ok!? ;)')

    Text_array_dinamico = '\n\033[1;31mOs arrays dinâmicos são bastante parecidos com os Arrays simples,\033[m \033[1;34ma principal característica que confere dinamismo diferencial a esses arrays é a capacidade de redimensionamento automático,\npermitindo a adição ou remoção de elementos de forma eficiente, sem a necessidade de especificar previamente o tamanho da lista.\nIsso proporciona flexibilidade significativa em comparação com arrays simples. À medida que novos elementos são adicionados, a lista pode expandir automaticamente para acomodar o crescimento dinâmico dos dados, simplificando o gerenciamento de coleções de informações de tamanho variável.\nNo entanto,  essa flexibilidade pode implicar em um pequeno custo de desempenho em comparação com estruturas de dados mais especializadas para operações específicas.\033[m'
    Text_lista_encadeada = '\n\033[1;31mA lista encadeada é uma estrutura de dados que consiste em nós,\033[m \033[1;34monde cada nó contém um valor e uma referência ao próximo nó na sequência. Ao contrário das listas padrão, as listas encadeadas não exigem um espaço contínuo de memória, o que facilita a inserção e remoção eficientes de elementos em qualquer posição. Cada nó é composto por dois campos: um para armazenar o valor do elemento e outro para apontar para o próximo nó na lista. O último nó geralmente aponta para um valor nulo, indicando o final da lista. As listas encadeadas oferecem vantagens em cenários onde a manipulação frequente de inserções e remoções é necessária, uma vez que essas operações podem ser realizadas em tempo constante, ao contrário de estruturas de dados como arrays, onde essas operações podem ter complexidade linear. No entanto, o acesso aleatório aos elementos pode ser menos eficiente em comparação com arrays, uma vez que é necessário percorrer a lista sequencialmente a partir do início ou do final.\033[m'
    Text_array = '\n\033[1;31mO array é uma estrutura básica mas muito acessível e versátil!\n\033[m\033[1;34mA implementação e manipulação não é tão difícil quanto as de outras estruturas.\nAs operações de acesso aos elementos por índices são eficientes, proporcionando um acesso rápido e direto à informação desejada. \nMas atenção!! Existem algumas desvantagens ao se utilizar arrays. O consumo de memória pode ser uma preocupação, especialmente ao lidar com grandes conjuntos de dados, uma vez que as listas podem consumir mais espaço do que estruturas de dados mais especializadas.\033[m'

    print(f'{Text_array}\n\n {Text_array_dinamico}\n\n {Text_lista_encadeada}\n\n')
    

    Pergunta_lista  = int(input('\n\nSe o array simples for o melhor para o seu projeto, digite 1. Se o array dinâmico for o melhor, digite 2. E caso a lista encadeada seja a melhor, digite 3.\n'))
    condic_1 = 0
    Resultado_list = 0

    def pergunta1(Pergunta_lista, condic_1, Resultado_list):
        while condic_1 != True:
            if 4 > Pergunta_lista > 0 :
                condic_1 = True
                Resultado_list = Pergunta_lista
                break
            else:
                Pergunta_lista = int(input('Inserir um valor valido!\n'))
                pergunta1(Pergunta_lista, condic_1, Resultado_list)
            
        if Resultado_list == 1:
            print('Parabéns, o array simples é a estrutura de dados certa pra vc! Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
            quit()
        elif Resultado_list == 2:
            print('Parabéns, o array dinâmico é a estrutura de dados certa pra vc! Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
            quit()
        elif Resultado_list == 3:
            print('Parabéns, o array simples é a estrutura de dados certa pra vc! Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
            quit()

    pergunta1(Pergunta_lista, condic_1, Resultado_list)
    
    
    
    
def implemente_pilha():
    print('\n\033[1;33mPara fazer a implementação, siga os passos:\033[m\n\n')
    
    print('''\n\033[1;31m#Crie a calsse pilha\033[m
        class Pilha:  

\n\033[1;31m#Crie a função init para inicializar a pilha como uma lista vazia\033[m
    def init(self):  
        self.itens = []

\n\033[1;31m#Crie uma função para verificar se a pilha está vazia\033[m
    def esta_vazia(self):  
        return len(self.itens) == 0

\n\033[1;31m#Crie uma função para adicionar itens ao topo da pilha\033[m
    def empilhar(self, item):  
        self.itens.append(item)
        print(f"{item} foi empilhado na pilha.")

\n\033[1;31m#Crie uma função para remover um item e retornar o item no topo da pilha\033[m
def desempilhar(self):  
        if not self.esta_vazia():
            item_removido = self.itens.pop()
            print(f"{item_removido} foi desempilhado da pilha.")
            return item_removido
        else:
            print("A pilha está vazia. Nenhum item para desempilhar.")

\n\033[1;31m#Crie uma função para retornar o item no topo da pilha sem removê-lo\033[m
    def topo(self):  
        if not self.esta_vazia():
            return self.itens[-1]
        else:
            return None\n\n\n''')
    
    print('\n\033[1;33mDepois que fizer a implementação da pilha, utilize o código abaixo para testar.\n\n\033[m')

    print('''def tutorial_pilha():
        \n\033[1;31m# Função que exemplifica o uso da pilha\033[m
        pilha = Pilha()
        print("Implementação de uma Pilha em Python:")

        \n\033[1;31m# Empilhando alguns itens\033[m
        pilha.empilhar(10)
        pilha.empilhar(20)
        pilha.empilhar(30)

        \n\033[1;31m# Exibindo o topo da pilha\033[m
        print(f"Topo da pilha: {pilha.topo()}")

        \n\033[1;31m# Desempilhando alguns itens\033[m
        pilha.desempilhar()
        pilha.desempilhar()

        \n\033[1;31m# Exibindo o topo da pilha após desempilhar\033[m
        print(f"Topo da pilha após desempilhar: {pilha.topo()}")

        \n\033[1;31m# Desempilhando todos os itens restantes\033[m
        pilha.desempilhar()
        pilha.desempilhar()''')
    
    
def chama_fila():
    

    def imprimirEsporte():
        print('Esporte: ' + str(lb_esportes.get(ACTIVE)))

    def addEsporte():
        lb_esportes.insert(END, vnovoesporte.get())

    def removeEsporte():
        item_selecionado = lb_esportes.curselection()
        for item_selecionado in item_selecionado[::-1]:
            lb_esportes.delete(item_selecionado)

    lista = Tk()
    lista.title('Exemplo')
    lista.geometry('500x300')

    listaEsportes = ['Futebol', 'Vôlei', 'Basquete']

    lb_esportes=Listbox(lista)
    for esportes in listaEsportes:
        lb_esportes.insert(END, esportes)
    lb_esportes.pack()

    btn_esporte=Button(lista,text='Imprimir esporte',command=imprimirEsporte)
    btn_esporte.pack()

    vnovoesporte=Entry(lista)
    vnovoesporte.pack()
    btn_inseriresporte=Button(lista,text='Adicionar esporte',command=addEsporte)
    btn_inseriresporte.pack()

    btn_removeEsporte=Button(lista, text="delete",command=removeEsporte).pack()


    lista.mainloop()
#===================================================================================================================================

if total == 'Array':
    print('Resultado: o array é a estrutura de dados ideal para o seu projeto!')
    caso_lista()
elif total == 'Pilha':
    print('Resultado: a pilha é a estrutura de dados ideal para o seu projeto!') 
    print('Pilha é uma estrutura de dados fundamental caracterizada pelo modelo Last In, First Out (LIFO), onde o último elemento no topo da pilha. A flexibilidade das listas em Python permite uma implementação direta e intuitiva da estrutura de pilha, sendo útil em situações onde a ordem inversa de processamento de dados é crucial, como na inversão de texto. Veja como é feita a implementação da estrutura abaixo.')
    implemente_pilha()
elif total == 'Fila':
    print('Resultado: a fila é a estrutura de dados ideal para o seu projeto! Veja como essa estrura funciona abaixo. ')
    chama_fila()
    print('Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
elif total == 'Arvore':
    print('Resultado: a árvore é a estrutura de dados ideal para o seu projeto! árvores são estruturas de dados fundamentais que podem ser implementadas de diversas maneiras para modelar relações hierárquicas entre elementos. \nUma árvore consiste em nós organizados de forma hierárquica, com um nó principal chamado de raiz, de onde se originam os ramos conectados a outros nós, denominados filhos. Cada nó pode ter zero ou mais filhos, formando uma estrutura de árvore que é frequentemente utilizada em algoritmos de busca, estruturas de diretórios de arquivos, e na representação de estruturas organizacionais, entre outras aplicações.')
    print('Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
elif total == 'Grafo':
    print('Resultado: o grafo é a estrutura de dados ideal para o seu projeto! Em sua essência, um grafo consiste em nós (vértices) conectados por arestas, representando relações entre elementos.\nEssa estrutura pode ser construída utilizando estruturas de dados nativas, como dicionários para representar os nós e suas conexões. As arestas podem ser armazenadas como pares de nós em listas ou tuplas.\nEssa abordagem mais básica oferece flexibilidade na criação e manipulação de grafos, permitindo a implementação de algoritmos personalizados para percorrer, analisar e extrair informações de grafos, adaptando-se às necessidades específicas do problema em questão.')
    print('Chegamos ao final do seu questionário, para conhecer mais sobre a implementação dessa estrutura acesse o: https://github.com/GeovanaRamos/ed-cic-2023-2')
