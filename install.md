Autor: Daniel Selbach<br>
Instagram Daniel Selbach: https://www.instagram.com/danielselbachtechofc/<br>
YouTube Daniel Selbach: https://www.youtube.com/@danielselbachtechofc<br>
Linkedin Daniel Selbach: https://www.linkedin.com/in/danielselbachtech/<br>
Github Daniel Selbach: https://github.com/danielselbachtechofc<br>
Data de criação: 11/08/2024<br>




#01_ Primeira etapa: Verifique a Arquitetura do Sistema Operacional
```bash
A) Verificar a Arquitetura do Sistema Operacional: Clique no ícone da lupa no Windows e vá em "Sistema" e na aba "Tipo de Sistema", verifique se informa "Sistema operacional de 64 bits, processador baseado em x64" ou algo do tipo, validando que o seu sistema operacional é 64-bit.
```

#02_ Segunda etapa: Download da ISO do EVE-NG e Client do EVE-NG
```bash
A) Link de download do EVE-NG e Client EVE-NG: https://www.eve-ng.net/index.php/download/
B) Versão do download EVE-NG e Client EVE-NG: eve-ce-prod-6.2.0-4-full.iso / EVE-NG-Win-Client-Pack-2.0.exe (Link atualizado em 11/08/2024)
C) Arquitetura do Sistema Operacional: 64-bit
D) Tipo de instalação: DVD Image (ISO) Installer
```

#03_ Terceira etapa: Criação da Máquina Virtual no Oracle VirtualBOX
A) Link de download do Oracle VirtualBOX: https://www.virtualbox.org/wiki/Downloads

Oracle VirtualBOX Gerenciado (versão 7.x ou superior).

01) Ferramentas;	
<Novo>

02) Nome da Máquina Virtual e Sistema Operacional:
	Nome: eve-ng (altere conforme a sua necessidade)
	Pasta (F): #PATH_PADRÃO\eve-ng (altere conforme a sua necessidade)
	Imagem ISO: eve-ce-prod-6.2.0-4-full.iso
	Edição: (sem informação)
	Tipo: Linux
	Versão: Ubuntu (64-bit)
<Próximo>

03) Hardware:
	Memória Base: 4096MB (altere conforme a sua necessidade, mínimo 2048MB)
	Processadores: 02 CPU (altere conforme a sua necessidade, mínimo 2 CPU)
	Habilitar EFI (SOs especiais apenas): OFF (Desligado)
<Próximo>

04) Disco Rígido Virtual:
	Criar um novo disco rígido virtual agora: ON (Selecionar)
	  Tamanho do Disco: 25,00GB (alterar conforme a sua necessidade, mínimo 25GB)
	Pré-alocar Tamanho Total (F): OFF (Desativado) 
<Próximo>

05) Sumário
<Finalizar>
```

#04_ Quarta Etapa: Configurações da Máquina Virtual EVE-NG
```bash
Oracle VirtualBOX Gerenciado (versão 7.x ou superior).

01) Selecionar a Máquina Virtual: eve-ng
<Configurações>

02) Sistema
	Processador
      Recursos Estendidos: Habilitar PAE/NX
                           Habilitar VT-x/AMD-v Aninhado 
                           
03) Rede
	Adaptador 1 (LAN)
	  Habilitar Placa de Rede: ON (Habilitar)
	  Conectado a: Placa em modo Bridge
    Avançado: Permitir Tudo
	  Nome: Intel(R) Ethernet Connection (Placa de Rede On-Board)
	  #OBSERVAÇÃO: VERIFIQUE QUAL PLACA DE REDE VOCÊ ESTÁ USANDO NO SEU EQUIPAMENTO
	  #QUE ESTÁ CONECTADO NA SUA REDE LOCAL, PODE SER PLACA DE REDE CABEADA OU PLACA
	  #SEM-FIO (RECOMENDO SEMPRE PLACA DE REDE CABEADA, MELHOR DESEMPENHO).
<OK>
```

#05 Quinta Etapa: Instalação e Configuração do EVE-NG<br>
```bash
A) Instalação do EVE-NG: https://www.eve-ng.net/index.php/documentation/installation/virtual-machine-install/


