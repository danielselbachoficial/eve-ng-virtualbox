Autor: Daniel Selbach<br>
Instagram Daniel Selbach: https://www.instagram.com/danielselbachtechofc/<br>
YouTube Daniel Selbach: https://www.youtube.com/@danielselbachtechofc<br>
Linkedin Daniel Selbach: https://www.linkedin.com/in/danielselbachtech/<br>
Github Daniel Selbach: https://github.com/danielselbachtechofc<br>
Data de criação: 11/08/2024<br>


# Manual de instalação e configuração do EVE-NG no VirtualBOX 

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
```bash

01) Localize o arquivo do EVE-NG Client.

02) Execite p arquivo do EVE-NG Client.
<EVE-NG-Win-Client-Pack-2.0.exe>

03) Aceite os termos da instalação e clique em próximo durante o processo para concluir a instalação do EVE-NG Client.
```

#04_ Quarta etapa: Criação da Máquina Virtual no Oracle VirtualBOX
```bash

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

#05_ Quinta Etapa: Configurações da Máquina Virtual EVE-NG
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

#06 Sexta Etapa: Primeira parte da Instalação do EVE-NG<br>
```bash

A) Instalação do EVE-NG: https://www.eve-ng.net/index.php/documentation/installation/virtual-machine-install/

01) Selecionar a Máquina Virtual: eve-ng
<Iniciar>

02) Ao iniciar aperta a sequência de teclas: F12 > C > ENTER

03) Selecionar o idioma da sua preferência. Ex: Português (Brazil) ou English.

04) Selecione o layout do seu teclado. Ex: Portuguese, para teclados ABNT2 (PT-BR)

05) Clicar em "Concluído".

<ATENÇÃO NESTA PARTE!!!>
06) Ao aparecer uma mensagem, clique na opção "Continuar" para instalar o EVE-NG.

<OBS: Ao clicar em “NÃO” você vai instalar o sistema operacional Ubuntu, em vez do EVE-NG.>

07) Aguarde a finalização da instalação.
```

#07 Sétima Etapa: Segunda parte da Instalação do EVE-NG<br>
```bash

<ATENÇÃO NESTA PARTE!!!>
01) Quando informar a mensagem para solicitar a instalação novamente do EVE-NG, desligue a máquina virtual.
	1.1 Clique no "X" para fechar a Máquina Virtual.
		1.2 Marque a opção "Desligue a máquina".
			1.3 Clique em "OK".

02) Selecionar a Máquina Virtual: eve-ng
<Configurações>

03) Clicar em "Armazenamento"

04) Selecionar o dispositivo de armazenamento
	Controladora: IDE
		Selecionar a imagem ISO "eve-ce-prod-6.2.0-4-full.iso".
			Clicar com botão direito do mouse e clicar em "Remover Conexão" > "Remover".

05) Clicar em "OK".
```

#08 Oitava Etapa: Terceira parte da Instalação do EVE-NG<br>
```bash

01) Selecionar a Máquina Virtual: eve-ng
<Iniciar>

02) Aguarde a Máquina Virtual iniciar para inserir o usuário e senha padrão do EVE-NG.
<Usuário: root>
<Senha: eve>

03) Após usar o usuário e senha padrão do EVE-NG, vai aparecer uma mensagem perguntando se você quer alterar a senha root do EVE-NG, alterar o nome da máquina virtual, configurar IP via DHCP (Pode mudar) ou estático (Não muda), selecionar o servidor NTP, configurar o servidor Proxy.

<OBS: Se não quiser alterar nada nesta parte, aperte "ENTER" em todas as opções.>
```

#09 Nona Etapa: Acessando o EVE-NG no navegador de internet<br>
```bash

01) Abra o seu navegador de internet e digite o IP do seu EVE-NG.
Exemplo: 10.0.20.250

02) Digite o usuário e senha, após clique em "Sign in (Entrar) ou aperte a tecla ENTER".
<Usuário: admin>
<Senha: eve>

03) Criar um laboratório.
	1.1 Clicar no ícone de "documento" no menu abaixo de novo nome no lado esquerdo.
		1.2 Informar um nome para o laboratório.
			1.3 Clicar em salvar e aguardar o laboratório abrir.
```

#10 Décima Etapa: Adicionar um vendor novo no EVE-NG<br>
```bash
A) Link de download da imagem MikroTik: https://download.mikrotik.com/routeros/7.15.3/chr-7.15.3.vmdk.zip

01) Abrir o PowerShell ou CMD e acessar a Máquina Virtual do EVE-NG via SSH.
<ssh usuário@ip-da-eve-ng>
<Exemplo: ssh root@10.0.20.250>

02) Apos, informar a mensagem "Are you sure want to continue connecting (yes/no/[fingerprint])?" em inglês ou "Tem certeza de que deseja continuar conectando (sim/não/[impressão digital])?" em português.
	1.1 Digitar "yes ou sim" e apertar "ENTER".
		1.2 Digitar a senha do usuário e apertar "ENTER".

02) Agora, use os comandos abaixo para criar a imagem MikroTik dentro do EVE-NG.

<ATENÇÃO, FAÇA OS COMANDOS EM SEQUÊNCIA, NÃO PULE NENHUM COMANDO, CASO CONTRÁRIO NÃO FUNCIONARÁ!!!>

mkdir -p /opt/unetlab/addons/qemu/mikrotik-7.15.3

cd /opt/unetlab/addons/qemu/mikrotik-7.15.3

wget https://download.mikrotik.com/routeros/7.15.3/chr-7.15.3.vmdk.zip

unzip chr-7.15.3.vmdk.zip

/opt/qemu/bin/qemu-img convert -f vmdk -O qcow2 chr-7.15.3.vmdk hda.qcow2

/opt/unetlab/wrappers/unl_wrapper -a fixpermissions

rm -rf chr-7.15.3.vmdk
rm -rf chr-7.15.3.vmdk.zip
```


