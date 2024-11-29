<h1 align="left">androidbox app player</h1>

###

<h4 align="left">Requisitos<br><br>Sistema Operacional: Windows<br>Espaço em Disco: Aproximadamente 10 GB disponíveis</h4>

###

<h2 align="left">Funcionalidades</h2>

###

<p align="left">- **Emulação de Android**: Utiliza QEMU para rodar Android em um ambiente virtualizado.<br><br>- **Configuração Personalizável**: O usuário pode configurar a quantidade de RAM, o tamanho de armazenamento e o controle (Xbox 360, PS3, teclado).<br><br>- **Rede Privada**: Suporta configuração de rede privada com IP e porta personalizáveis.<br><br>- **Configurações Persistentes**: As configurações são salvas em arquivos JSON para persistir entre reinicializações.</p>

###

<p align="left">Download<br>Baixar o AndroidBox App Player<br>Você pode baixar a versão mais recente do AndroidBox App Player diretamente de:<br><br>Site Oficial do AndroidBox (caso o site tenha um link oficial de download)<br>Repositório no GitHub</p>

###

<h2 align="left">esse app foi feito com essas depedencias</h2>

###

<div align="left">
  <img src="https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=black&style=for-the-badge" height="40" alt="android logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge" height="40" alt="python logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/Android Studio-3DDC84?logo=androidstudio&logoColor=black&style=for-the-badge" height="40" alt="androidstudio logo"  />
  <img width="12" />
  <img src="https://img.shields.io/badge/Canva-00C4CC?logo=canva&logoColor=black&style=for-the-badge" height="40" alt="canva logo"  />
</div>

###

<h4 align="left">o android studio na verdade e qemu</h4>

###

<p align="left">configuração<br>Passo 1: Editar o Arquivo config.json<br>O arquivo config.json contém todas as configurações principais do emulador. Você pode abrir este arquivo com um editor de texto, como o Notepad++ ou o Visual Studio Code, e ajustar os parâmetros conforme necessário.<br><br>Exemplo do conteúdo do config.json:<br><br>json<br>Copiar código<br>{<br>  "ram_size": 2048,<br>  "storage_size": 8192,<br>  "control": "keyboard",<br>  "screen_full": false,<br>  "screen_size": "1024x768",<br>  "user_name": "Seu Nome"<br>}</p>

###

<p align="left">Aqui está o que cada campo faz:<br><br>ram_size: Tamanho da memória RAM em MB (exemplo: 2048 para 2 GB).<br>storage_size: Tamanho do armazenamento virtual para o emulador (em MB).<br>control: Tipo de controle a ser usado ("keyboard" para teclado, "xbox360" para controle Xbox, "ps3" para controle PS3).<br>screen_full: Defina como true para ativar o modo de tela cheia, ou false para usar uma janela redimensionada.<br>screen_size: Tamanho da tela em formato largura x altura (exemplo: "1024x768").<br>user_name: Nome do usuário que será exibido no título da janela do QEMU.</p>

###
