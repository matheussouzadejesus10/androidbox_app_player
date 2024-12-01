# SECURITY.md - Medidas de Segurança do Projeto AndroidboxAppPlayer

Este projeto foi desenvolvido com ênfase na segurança, garantindo que o código e os processos de execução sejam seguros e livres de vulnerabilidades comuns. A seguir estão as práticas de segurança adotadas:

## 1. Validação de Entradas

Todas as entradas e dados utilizados no programa são validados:

- **Arquivos JSON**: A leitura de arquivos `config.json` e `rede.json` é cuidadosamente validada. Caso o arquivo não exista ou seja corrompido, o programa falha de maneira controlada.
- **Portas e Configurações Aleatórias**: A configuração de rede (`rede.json`) gera uma porta aleatória segura para evitar qualquer comportamento predeterminado ou malicioso.

## 2. Execução Segura de Comandos com `subprocess.run()`

A execução de comandos do sistema (QEMU) é realizada de forma segura com a seguinte prática:
- **Listas de Argumentos**: Todos os comandos são passados como listas de argumentos. Isso impede a injeção de comandos maliciosos.
- **Sanitização de Dados**: O código utiliza uma abordagem de sanitização para garantir que nenhuma entrada indesejada ou vazia seja executada.

## 3. Controle de Acesso a Arquivos

O código verifica se os arquivos de configuração essenciais (como `android.qcow2`, `sdcard.img`, `data.img`) estão presentes antes de iniciar o processo, garantindo que o programa não falhe devido a arquivos ausentes.

## 4. Isolamento e Segurança de Rede

A configuração de rede utiliza redirecionamento de portas (via `hostfwd`) para garantir que a comunicação de rede ocorra de maneira controlada. Também há suporte para modo sandbox no QEMU, o que isola o emulador de outras partes do sistema operacional.

## 5. Execução Segura e Configuração do PyInstaller

O PyInstaller é utilizado para criar o executável de forma segura:
- **Sem UPX**: Não utilizamos a compactação UPX para evitar problemas com antivírus.
- **Ícone Personalizado**: O ícone do aplicativo é configurado corretamente para identificação visual.
- **Sem Console de Texto**: O programa é executado em uma janela gráfica, sem a exposição de informações desnecessárias no terminal.

## 6. Gerenciamento de Logs

Logs são gerados durante a execução do emulador para fins de diagnóstico. O arquivo de log é armazenado em um diretório específico e pode ser acessado para monitoramento.

## 7. Atualizações e Manutenção

Manter o código e as dependências do projeto atualizados é fundamental. Por favor, consulte as instruções do repositório para quaisquer atualizações de segurança.

---

## Aviso Importante

Este código é projetado para ser executado localmente, com foco em garantir a segurança e integridade dos dados do usuário. Se você deseja implantar este projeto em um servidor ou em ambiente de produção, é recomendado revisar a segurança de rede e realizar auditorias regulares.

Se você tiver dúvidas ou sugestões sobre as práticas de segurança, entre em contato com os desenvolvedores.

