import PySimpleGUI as sg
import speech_recognition as sr
import pyttsx3
import tkinter
from tkinter import *
from tkinter import ttk

engine = pyttsx3.init()
engine.say(
    "olá me chamo Ruby. Eu sou uma inteligência artificial programado para ajudar pessoas!")
engine.runAndWait()
engine.say("eu posso  fazer contas basicas, adicionar interesse de curso , e contar histórias e escoler o melhor celular para o seu dia . Estou aprendendo cada dia mais! ")
engine.runAndWait()
engine. say(" Qual é seu nome?")
engine.runAndWait()

nome = input("digite o  seu nome ")

print(nome)

engine.say('MUITO PRAZER')


engine.say(nome)
engine.runAndWait()

engine.say("o que você gostaria de fazer?")
engine.runAndWait()

engine.say("escolha um das opição abaixo ")
engine.runAndWait()

engine.say("gostaria de fazer calculos digite 1")
engine.runAndWait()
print("digite 1 para opçao calculadora")

engine.say("gostaria de  adicionar interesse de curso em nossa lista")
engine.runAndWait()
print("digite 2 para opçao para adicionar interesse de curso  em nossa lista ")

engine.say("para escultar história digite 3")
engine.runAndWait()
print("digite 3 para opçao para escutar história")

engine.say(
    "digite 4 para  escolhar o  melhor celular e seu notebook para o seu dia via telegram ")
engine.runAndWait()
print("digite 4 para  escolhar o  melhor celular e seu pc para o seu dia via telegram ")

engine.say("digite 6 para jogar  o jogo  da velha")
engine.runAndWait()
print("digite 6 para jogar  o jogo  da velha ")

opçao = int(input("digite sua escolha:"))

if opçao == 1:
    print("operaçao calculadora")

    engine .say("digite o primeiro número:")
    engine.runAndWait()
    num_a = input("digite o primeiro número:")
    engine.say("digite o segundo número:")
    engine.runAndWait()
    num_b = input("digite o segundo número:")

    num_a = int(num_a)
    num_b = int(num_b)

    engine.say("digite a operação desejada")
    engine.runAndWait()
    print("digite a opeção desejada")
    engine.say(
        "digite 1 para somar; digite2 para subtrair digite 3 para multiplicar , digite 4 para dividir ")
    engine.runAndWait()
    operaçao = input(
        "digite 1 para somar;\ndigite 2 para subtrair;\ndigite 3 para multiplica;\ndigite 4 para dividir")

    if operaçao == "1":
        print("soma é", num_a+num_b)
        engine.say("a soma foi realizada com  sucesso")
        engine.runAndWait()

    elif operaçao == "2":
        print("a subtração é", num_a-num_b)
        engine.say("a soma foi realizada com  sucesso")
        engine.runAndWait()

    elif operaçao == "3":
        print("a multiplicação é:", num_a*num_b)
        engine.say("a multiplicação foi realizada com  sucesso")
        engine.runAndWait()

    elif operaçao == "4":
        print("a diviçao é:", num_a*num_b)
        engine.say("a divição foi realizada com sucesso")
        engine.runAndWait()

        engine.say("obrigado por fazer a operação matematica")
        engine.runAndWait()

    if opçao == 2:
        print("adicinar  interesse de curso  em nossa lista")
        engine.say("adicinar enterecer de curso  em nossa lista")
        engine.runAndWait()


def criar_janela():
    sg.theme('DarkBlue4')
    linha = [
            [sg.Checkbox(''), sg.Input('')]
    ]

    layout = [
        [sg.Frame('adicionar  interesse de curso',
                  layout=linha, key='container')],
        [sg.Button('Novo curso'), sg.Button('Resetar')]
    ]

    return sg.Window('Gerenciador de interesse  de curso', layout=layout, finalize=True)


# Criar a Janela
janela = criar_janela()

while True:
    event, values = janela.read()
    if event == sg.WIN_CLOSED:
        break
    elif event == 'Novo curso':
        janela.extend_layout(janela['container'], [
                             [sg.Checkbox(''), sg.Input('')]])
    elif event == 'Resetar':
        janela.close()
        janela = criar_janela()


if opçao == 3:
    engine.say("qual história você gostaria de escultar? ")
    engine.runAndWait()
    print("qual história você gostaria de escultar ?")
    engine.say("digite 1 para escultar a hisória do senai?\ndigite 2 para  escultar a história do 5G?\ndigite 3 para escultar a  historia da Samsung?\ndigite 4 para escultar a história da inteligência artificial\ndigite 5 para escultar a história da ecologia ")
    engine.runAndWait()
    operaçao = input("digite 1 para escultar a hisória do senai?\ndigite 2 para  escultar a história do 5G?\ndigite 3 para escultar a  historia da Samsung?\ndigite 4 para escultar a história da inteligência artificial\ndigite 5 para escultar a história da ecologia ")

    if operaçao == "1":
        engine.say("Criado em 22 de janeiro de 1942, pelo decreto-lei 4.048 do então presidente Getúlio Vargas, o Senai - Serviço Nacional de Aprendizagem Industrial - surgiu para atender a uma necessidade premente: a formação de profissionais qualificados para a incipiente indústria de base. Já na ocasião, estava claro que sem educação profissional não haveria desenvolvimento industrial para o País."
                   "É uma entidade de direito privado organizado pelo empresariado industrial, através da CNI - Confederação Nacional da Indústria e pelas federações de indústrias nos estados."
                   "No Paraná, instalou-se em 12 de março de 1943 e é uma entidade do Sistema Fiep - Federação das Indústrias do Estado do Paraná. Desde sua criação, vem contribuindo com o crescimento da indústria e da comunidade paranaense.")
    engine.runAndWait()

    if operaçao == "2":
        engine.say("Foram quase 10 anos entre a banda larga e o 1° smartphone e um tempo muito menor até que uma tecnologia tão robusta fosse desenvolvida."
                   "como a que está em processo de implantação em todo o Brasil. O 4G entrou em funcionamento no início de 2010."
                   "Maior largura de banda, melhor qualidade de ligação, uma conexão mais rápida e estável. Muitas tecnologias avançaram graças"
                   "ao advento do 4G, como jogos, serviços de nuvem (cloud computing), plataformas de streaming e video on demand (VOD)."
                   "O 5G, contudo, já estava em elaboração na mesma época. Foi uma busca incessante por uma rede móvel com maior capacidade de conexão e que fosse além,"
                   "e que fosse além,  como é a Internet das Coisas (IoT), em que se aproveita tudo das redes móveis"
                   "como transporte, telemedicina, agricultura e educação.")
        engine.runAndWait()
    if operaçao == "3":
        engine.say("A Samsung nasceu na Coreia do Sul em 1938 e se transformou em um dos maiores conglomerados do país e do mundo, com atuação em diversas áreas"
                   "Apesar da diversidade dos negócios, ela é mais conhecida globalmente pelos eletrônicos"
                   "Fundada por Lee Byung-chul, a empresa teve origens modestas, dedicada à exportação de alimentos.")
        engine.runAndWait()

    if operaçao == "4":
        engine.say("Na tecnologia, a Inteligência Artificial é a inteligência demonstrada por máquinas ao executar tarefas complexas associadas a seres inteligentes, além de também ser um campo de estudo acadêmico, onde seu principal objetivo é de executar funções de modo autônomo.")
        engine.runAndWait()

    if operaçao == "5":
        engine.say("A palavra ecologia (do grego oikos, casa foi cunhada no século XIX pelo zoólogo alemão Ernst Haeckel, para designar a relação dos animais com seu meio ambiente orgânico e inorgânico. A expressão meio ambiente inclui tanto outros organismos quanto o meio físico circundante.")
        engine.runAndWait()
if opçao == 6:
    # cores ---------------------------------------
    co0 = "#FFFFFF"  # branca / white
    co1 = "#333333"  # preta pesado / dark black
    co2 = "#fcc058"  # laranja / orange
    co3 = "#38576b"  # valor / value
    co4 = "#3297a8"   # azul / blue
    co5 = "#fff873"   # amarela / yellow
    co6 = "#fcc058"  # laranja / orange
    co7 = "#e85151"   # vermelha / red
    co8 = co4   # + verde
    co10 = "#fcfbf7"
    fundo = "#3b3b3b"  # preta / black

# criando janela principal
    janela = Tk()
    janela.title('')
    janela.geometry('260x370')
    janela.configure(bg=fundo)


# Dividindo a janela em 2 frames ---------------------------------------

    frame_cima = Frame(janela, width=240, height=100, bg=co1, relief="raised")
    frame_cima.grid(row=0, column=0, sticky=NW, padx=10, pady=10)

    frame_baixo = Frame(janela, width=240, height=300, bg=fundo, relief="flat")
    frame_baixo.grid(row=1, column=0, sticky=NW)


# Configurando o frame cima ---------------------------------------
    app_x = Label(frame_cima, text='X', height=1, relief='flat',
                  anchor='center', font=('Ivy 40 bold'), bg=co1, fg=co7)
    app_x.place(x=25, y=10)
    app_x = Label(frame_cima, text='Jogador 1', height=1, relief='flat',
                  anchor='center', font=('Ivy 7 bold'), bg=co1, fg=co0)
    app_x.place(x=17, y=70)
    app_x_pontos = Label(frame_cima, text='0', height=1, relief='flat',
                         anchor='center', font=('Ivy 30 bold'), bg=co1, fg=co0)
    app_x_pontos.place(x=80, y=20)

    app_separador = Label(frame_cima, text=':', height=1, relief='flat',
                          anchor='center', font=('Ivy 30 bold'), bg=co1, fg=co0)
    app_separador.place(x=110, y=20)

    app_o = Label(frame_cima, text='O', height=1, relief='flat',
                  anchor='center', font=('Ivy 40 bold'), bg=co1, fg=co4)
    app_o.place(x=170, y=10)
    app_o = Label(frame_cima, text='Jogador 2', height=1, relief='flat',
                  anchor='center', font=('Ivy 7 bold'), bg=co1, fg=co0)
    app_o.place(x=165, y=70)
    app_o_pontos = Label(frame_cima, text='0', height=1, relief='flat',
                         anchor='center', font=('Ivy 30 bold'), bg=co1, fg=co0)
    app_o_pontos.place(x=130, y=20)

# Configurando o frame baixo ---------------------------------------


# Criando logica do app ---------------------------------------

    jogador_1 = "X"
    jogador_2 = "O"

    score_1 = 0
    score_2 = 0

    tabela = [['1', '2', '3'], ['4', '5', '6'], ['7', '8', '9']]

    jogando = 'X'
    joga = ''
    contador = 0
    contador_de_rodada = 0

    def iniciar_jogo():
        b_jogar.place(x=800, y=350)
    # pra controlar o jogo

    def controlar(i):
        global jogando
        global contador
        global jogar

        # comparando o valor recebido
        if i == str(1):
            # verificando se aquela posicao esta vazia ou nao
            if b_0['text'] == '':
                # verificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_0['fg'] = cor
                b_0['text'] = jogando
                tabela[0][0] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(2):
            # verificando se aquela posicao esta vazia ou nao
            if b_1['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_1['fg'] = cor
                b_1['text'] = jogando
                tabela[0][1] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(3):
            # verificando se aquela posicao esta vazia ou nao
            if b_2['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_2['fg'] = cor
                b_2['text'] = jogando
                tabela[0][2] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(4):
            # verificando se aquela posicao esta vazia ou nao
            if b_3['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_3['fg'] = cor
                b_3['text'] = jogando
                tabela[1][0] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(5):
            # verificando se aquela posicao esta vazia ou nao
            if b_4['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_4['fg'] = cor
                b_4['text'] = jogando
                tabela[1][1] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(6):
            # verificando se aquela posicao esta vazia ou nao
            if b_5['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_5['fg'] = cor
                b_5['text'] = jogando
                tabela[1][2] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(7):
            # verificando se aquela posicao esta vazia ou nao
            if b_6['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_6['fg'] = cor
                b_6['text'] = jogando
                tabela[2][0] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(8):
            # verificando se aquela posicao esta vazia ou nao
            if b_7['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_7['fg'] = cor
                b_7['text'] = jogando
                tabela[2][1] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        if i == str(9):
            # verificando se aquela posicao esta vazia ou nao
            if b_8['text'] == '':
                # varificando quem esta jogar e assim definir a cor do smbolo
                if jogando == 'X':
                    cor = co7
                if jogando == 'O':
                    cor = co8

                # definindo a cor do text do botao
                # e marcar aquela posicao da tabela
                # com o valor do jogador atual
                b_8['fg'] = cor
                b_8['text'] = jogando
                tabela[2][2] = jogando

                # verificando quem esta a jogar ,
                # para poder trocar de jogador
                if jogando == 'X':
                    jogando = 'O'
                    joga = 'Jogador 1'
                else:
                    jogando = 'X'
                    joga = 'Jogador 2'

                # incrementar o contador para proxima rodada
                contador += 1

        # Apos o contador ser maior ou igual a 5,
        # verifica se ouve algum vencedor de acordo
        # com os padroes seguintes dentro da tabela
        if contador >= 5:
            # linhas
            if tabela[0][0] == tabela[0][1] == tabela[0][2] != "":
                vencedor(jogando)
            elif tabela[1][0] == tabela[1][1] == tabela[1][2] != "":
                vencedor(jogando)
            elif tabela[2][0] == tabela[2][1] == tabela[2][2] != "":
                vencedor(jogando)

            # colunas
            if tabela[0][0] == tabela[1][0] == tabela[2][0] != "":
                vencedor(jogando)
            elif tabela[0][1] == tabela[1][1] == tabela[2][1] != "":
                vencedor(jogando)
            elif tabela[0][2] == tabela[1][2] == tabela[2][2] != "":
                vencedor(jogando)

            # diagonais
            if tabela[0][0] == tabela[1][1] == tabela[2][2] != "":
                vencedor(jogando)
            elif tabela[0][2] == tabela[1][1] == tabela[2][0] != "":
                vencedor(jogando)

            # Empate
            if contador >= 9:
                vencedor('Foi empate')

    # pra decidir o vencedor

    def vencedor(i):
        global tabela
        global score_1
        global score_2
        global contador_de_rodada
        global contador

        # bloqueando os botoes
        b_0['state'] = 'disable'
        b_1['state'] = 'disable'
        b_2['state'] = 'disable'
        b_3['state'] = 'disable'
        b_4['state'] = 'disable'
        b_5['state'] = 'disable'
        b_6['state'] = 'disable'
        b_7['state'] = 'disable'
        b_8['state'] = 'disable'

        app_vencedor = Label(frame_baixo, text='', width=17, relief='flat',
                             anchor='center', font=('Ivy 13 bold'), bg=co1, fg=co2)
        app_vencedor.place(x=40, y=220)

        if i == 'X':
            score_2 += 1
            app_vencedor['text'] = 'Joagador 2 venceu'
            app_o_pontos['text'] = score_2

        if i == 'O':
            score_1 += 1
            app_vencedor['text'] = 'Joagador 1 venceu'
            app_x_pontos['text'] = score_1

        if i == 'Foi empate':
            app_vencedor['text'] = 'Foi um empate'

        def start():
            # limpando os botoes
            b_0['text'] = ''
            b_1['text'] = ''
            b_2['text'] = ''
            b_3['text'] = ''
            b_4['text'] = ''
            b_5['text'] = ''
            b_6['text'] = ''
            b_7['text'] = ''
            b_8['text'] = ''

            b_0['state'] = 'normal'
            b_1['state'] = 'normal'
            b_2['state'] = 'normal'
            b_3['state'] = 'normal'
            b_4['state'] = 'normal'
            b_5['state'] = 'normal'
            b_6['state'] = 'normal'
            b_7['state'] = 'normal'
            b_8['state'] = 'normal'

            app_vencedor.destroy()
            b_jogar.destroy()

        # Botao jogar
        b_jogar = Button(frame_baixo, command=start, text='Proxima rodada', height=1,  font=(
            'Ivy 10 bold'), overrelief=RIDGE, relief='raised', bg=fundo, fg=co0)
        b_jogar.place(x=70, y=197)

        def jogo_acabou():
            b_jogar.destroy()
            app_vencedor.destroy()

            terminar()

        if contador_de_rodada >= 5:
            jogo_acabou()
        else:
            contador_de_rodada += 1
            # reiniciando a tabela
            tabela = [['1', '2', '3'], ['4', '5', '6'], ['7', '8', '9']]
            contador = 0

    # pra terminar o jogo atual

    def terminar():
        global tabela
        global contador_de_rodada
        global score_1
        global score_2
        global contador

        tabela = [['1', '2', '3'], ['4', '5', '6'], ['7', '8', '9']]
        contador_de_rodada = 0
        score_1 = 0
        score_2 = 0
        contador = 0

        # bloqueando os botoes
        b_0['state'] = 'disable'
        b_1['state'] = 'disable'
        b_2['state'] = 'disable'
        b_3['state'] = 'disable'
        b_4['state'] = 'disable'
        b_5['state'] = 'disable'
        b_6['state'] = 'disable'
        b_7['state'] = 'disable'
        b_8['state'] = 'disable'

        app_fim = Label(frame_baixo, text='Jogo Acabou', width=17, relief='flat',
                        anchor='center', font=('Ivy 13 bold'), bg=co1, fg=co2)
        app_fim.place(x=25, y=90)

        # jogar de novo

        def jogar_denovo():
            app_x_pontos['text'] = '0'
            app_o_pontos['text'] = '0'
            app_fim.destroy()
            b_jogar.destroy()

            # chamando a funcao iniciar o jogo
            iniciar_jogo()

        # Botao jogar denovo
        b_jogar = Button(frame_baixo, command=jogar_denovo, text='Jogar de novo', height=1,  font=(
            'Ivy 10 bold'), overrelief=RIDGE, relief='raised', bg=fundo, fg=co0)
        b_jogar.place(x=80, y=197)

    # linhas verticais
    app_ = Label(frame_baixo, text='', height=23, relief='flat',
                 pady=5, anchor='center', font=('Ivy 5 bold'), bg=co0, fg=co7)
    app_.place(x=90, y=15)
    app_ = Label(frame_baixo, text='', height=23, relief='flat',
                 pady=5, anchor='center', font=('Ivy 5 bold'), bg=co0, fg=co7)
    app_.place(x=157, y=15)

    # linhas horizontais
    app_ = Label(frame_baixo, text='', width=46, relief='flat', padx=2,
                 pady=1, anchor='center', font=('Ivy 5 bold'), bg=co0, fg=co7)
    app_.place(x=30, y=63)
    app_ = Label(frame_baixo, text='', width=46, relief='flat', padx=2,
                 pady=1, anchor='center', font=('Ivy 5 bold'), bg=co0, fg=co7)
    app_.place(x=30, y=127)

    # linha 0
    b_0 = Button(frame_baixo, command=lambda: controlar('1'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_0.place(x=30, y=15)
    b_1 = Button(frame_baixo, command=lambda: controlar('2'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_1.place(x=96, y=15)
    b_2 = Button(frame_baixo, command=lambda: controlar('3'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_2.place(x=163, y=15)

    # linha 1
    b_3 = Button(frame_baixo, command=lambda: controlar('4'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_3.place(x=30, y=75)
    b_4 = Button(frame_baixo, command=lambda: controlar('5'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_4.place(x=96, y=75)
    b_5 = Button(frame_baixo, command=lambda: controlar('6'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_5.place(x=163, y=75)

    # linha 2
    b_6 = Button(frame_baixo, command=lambda: controlar('7'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_6.place(x=30, y=135)
    b_7 = Button(frame_baixo, command=lambda: controlar('8'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_7.place(x=96, y=135)
    b_8 = Button(frame_baixo, command=lambda: controlar('9'), text='', width=3, height=1,  font=(
        'Ivy 20 bold'), overrelief=RIDGE, relief='flat', bg=fundo, fg=co7)
    b_8.place(x=163, y=135)

# Botao jogar
    b_jogar = Button(frame_baixo, command=iniciar_jogo, text='Jogar', width=10, height=1,  font=(
        'Ivy 10 bold'), overrelief=RIDGE, relief='raised', bg=fundo, fg=co0)
    b_jogar.place(x=85, y=197)

    janela.mainloop()
