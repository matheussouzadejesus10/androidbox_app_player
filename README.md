# AndroidboxAppPlayer

O **AndroidboxAppPlayer** é um emulador Android de alta performance que usa o QEMU para simular dispositivos Android. Este repositório oferece uma aplicação empacotada para facilitar a execução do emulador sem a necessidade de configuração manual de dependências ou ambientes de desenvolvimento.

## Requisitos

Você só precisa instalar o **AndroidboxAppPlayer Installer** no site oficial ou GitHub. A aplicação já inclui tudo o que você precisa para rodar o emulador.

### Como instalar

1. **Baixe o instalador do site oficial ou do GitHub**:
   - [Site Oficial](https://androidboxemulador.blogspot.com/)
   - [Repositório no GitHub](https://github.com/matheussouzadejesus10/androidbox_app_player)

2. **Execute o instalador**:
   - O instalador irá configurar o emulador e todos os arquivos necessários automaticamente.mas va para a parte "Como configurar e executar"
 Como configurar e executar 

- **Emulador Android** utilizando **QEMU**.
- Suporte para gráficos acelerados com VirtIO.
- Suporte para dispositivos USB, incluindo controle Xbox 360, PS3 e teclado.
- Suporte para câmera (caso configurado no arquivo `config.json`).
- Configurações de rede com porta ADB personalizada.
- Logs gerados para monitoramento da execução do QEMU.

### Como configurar e executar

1. **Configuração do arquivo `config.json`**:
   
   O arquivo `config.json` contém as configurações do emulador, como quantidade de RAM, número de núcleos de CPU, controle de entrada, resolução da tela, entre outros.

   Exemplo do arquivo `config.json`:

   ```json
   {
     "ram_size": 2048,
     "cpu_cores": 2,
     "fullscreen": false,
     "screen_size": "1280x720",
     "control": "xbox360", //xbox360,ps3,keyboard
     "camera": true,
     "camera_front": false
   }

