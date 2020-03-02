# CRUD-Concession-ria-Python
CRUD Concessionária | Python


ListaCarros = []

while(True):

  print("\n[X]Olá, bem vindo ao Crud de Concessionaria!")
  print("[1]Cadastrar.")
  print("[2]Apresentar.")
  print("[3]Alterar.")
  print("[4]Excluir.")
  print("[5]Sair.")
  VerificadorMenu = str(input("[X]Escolha uma opção: "));

  if(VerificadorMenu == "1"):
    print("\n[X]Opção de Cadastrar")

    Codigo = str(input("[X]Digite o codigo do carro: "))
    Nome = str(input("[X]Digite o nome do carro: "))
    Ano = str(input("[X]Digite o ano do carro: "))
    Combustivel = str(input("[X]Digite o tipo de combustivel do carro: "))
    Configuração = str(input("[X]Digite a configuração do carro: "))
    Lugares = str(input("[X]Digite a quantidade de lugares do carro: "))
    Tração = str(input("[X]Digite o tipo de tração do carro: "))

    DadosCadastro = ("[ " + Codigo + " | " + Nome + " | " + Ano + " | " + Combustivel + " | " + Configuração + " | " + Lugares + " | " + Tração + " ]")

    ListaCarros.append(DadosCadastro)

  elif(VerificadorMenu == "2"):
    print("\n[X]Opção de Apresentar")

    TamanhoLista = len(ListaCarros)

    if(TamanhoLista == 0):
      print("[X]Nenhum usuário registrado!")

    else:
      for Contador in range(TamanhoLista):
        print("[X]Carro: " + str(Contador) + " - " + ListaCarros[Contador])


  elif(VerificadorMenu == "3"):
    print("\n[X]Opção de Alterar")

    TamanhoLista = len(ListaCarros)

    if(TamanhoLista == 0):
      print("[X]Nenhum usuário registrado!")

    else:
      CodigoAlterar = int(input("[X]Digite o carro a ser alterado: "))

      VerificaContador = 0

      for Contador in range(TamanhoLista):

        if(CodigoAlterar == Contador):
          VerificaContador = VerificaContador + 1

        else:
          VerificaContador = VerificaContador + 0

      if(VerificaContador > 0):
        
        Codigo = str(input("[X]Digite o codigo do carro: "))
        Nome = str(input("[X]Digite o nome do carro: "))
        Ano = str(input("[X]Digite o ano do carro: "))
        Combustivel = str(input("[X]Digite o tipo de combustivel do carro: "))
        Configuração = str(input("[X]Digite a configuração do carro: "))
        Lugares = str(input("[X]Digite a quantidade de lugares do carro: "))
        Tração = str(input("[X]Digite o tipo de tração do carro: "))

        DadosCadastro = ("[ " + Codigo + " | " + Nome + " | " + Ano + " | " + Combustivel + " | " + Configuração + " | "        + Lugares + " | " + Tração + " ]")

        ListaCarros[CodigoAlterar] = DadosCadastro

      else:
        print("[X]Carro inexistente")

  elif(VerificadorMenu == "4"):
    print("\n[X]Opção de Excluir")

    TamanhoLista = len(ListaCarros)

    if(TamanhoLista == 0):
      print("[X]Nenhum usuário registrado!")

    else:
      Codigo = int(input("[X]Digite o carro a ser excluido: "))

      VerificaContador = 0

      for Contador in range(TamanhoLista):
        
        if(Codigo == Contador):
          VerificaContador = VerificaContador + 1

        else:
          VerificaContador = VerificaContador + 0
      
      if(VerificaContador > 0):
        del ListaCarros[Codigo]
        print("[X]Carro: " + str(Contador) + " - Removido!")

      else:
        print("[X]Carro inexistente!")

  elif(VerificadorMenu == "5"):
    print("\n[X]Opção de Sair. Obrigado!")
    exit()

  else:
    print("\n[X]Escolha uma opção válida!")
