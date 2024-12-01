# AndroidBox App Player

O **AndroidBox App Player** é um emulador de Android para sistemas Windows, projetado para simular um ambiente Android no seu computador. Ele utiliza QEMU para emulação e PyInstaller para empacotar a aplicação.

## Funcionalidades do Simulador:

- **Emulação de Android**: Execute aplicativos Android em um ambiente virtualizado.
- **Suporte a Controle**: Conecte controles como **Xbox 360** ou **PS3**.
- **Câmera Virtual**: Suporte a câmeras USB para captura de vídeo.
- **Rede ADB**: Configuração automática de porta para comunicação ADB.
- **Logs e Monitoramento**: Geração de logs para rastrear erros e mensagens do QEMU.
- **Personalização**: Personalize o ícone do emulador e o nome da janela.

## Instalação:

### 1. Instale o Installer:
Baixe o **installer.exe** no [site oficial do AndroidBox App Player](https://github.com/matheussouzadejesus10/androidbox_app_player/releases) e siga os passos para instalar o emulador em seu computador.

### 2. Executando o Emulador:
Após a instalação, execute o **AndroidBox App Player** através do atalho criado no seu desktop. A aplicação irá iniciar automaticamente o emulador Android com as configurações padrão.

## Requisitos:

O instalador já inclui todos os componentes necessários, então **não é necessário instalar nenhum software adicional**. O pacote contém:

- **QEMU** (incluso no pacote)
- **PyInstaller** (para empacotar a aplicação)
- **Python 3.x** (somente necessário se você quiser executar o código-fonte)

## Uso:

1. **Configurações**: O emulador usa um arquivo de configuração chamado `config.json` para armazenar as preferências, como o tamanho da memória RAM e o controle a ser usado (Xbox, PS3, ou teclado).
   
2. **Emulação de Android**: O emulador irá carregar uma imagem do Android e iniciar a simulação automaticamente. Você pode interagir com o sistema Android através da tela do emulador ou conectar um controle.

3. **Log de Erros**: O aplicativo mantém um log detalhado das operações do QEMU em `logs/qemu-log.txt`, para diagnosticar problemas caso ocorram.

## Contribuições

Se você quiser contribuir para o projeto, sinta-se à vontade para enviar um **pull request** no GitHub. 

Certifique-se de testar as alterações antes de submeter.

## Licença

Este projeto está licenciado sob a **MIT License** - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**AndroidBox App Player** - Criado para facilitar a emulação de Android no desktop de forma rápida e eficiente.
