# Segurança no AndroidBoxAppPlayer

Este documento descreve as práticas de segurança e os cuidados que foram tomados no desenvolvimento do **AndroidBoxAppPlayer** (app.exe). Nosso objetivo é garantir que o aplicativo seja seguro, fácil de usar e que os dados dos usuários sejam protegidos.

## 1. Objetivo
O **AndroidBoxAppPlayer** é um emulador Android executado com QEMU. A segurança do aplicativo foi projetada para minimizar riscos de vulnerabilidades e manter a integridade do sistema.

## 2. Boas Práticas de Segurança Implementadas

### 2.1. **Validação de Entradas**
Todas as entradas do usuário e arquivos de configuração são validadas para garantir que valores maliciosos ou errôneos não sejam executados. Isso inclui a verificação de:
- Tamanhos de arquivos e valores válidos de armazenamento.
- Caminhos de arquivos de configuração e outros parâmetros.

### 2.2. **Uso de Subprocesso Seguro**
Ao executar o emulador QEMU, o comando é passado de forma segura utilizando `subprocess.run()` com um filtro para garantir que não existam parâmetros vazios ou indesejados. A execução de comandos de terminal é controlada rigorosamente.

```python
comando_seguro = [arg for arg in comando if arg]
subprocess.run(comando_seguro, check=True)
