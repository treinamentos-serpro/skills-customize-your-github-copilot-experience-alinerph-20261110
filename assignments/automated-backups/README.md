# 📘 Atividade: Backups Automatizados com Verificação

## 🎯 Objetivo

Crie um script Python que faça cópias de backup sem alterar os arquivos originais e confirme se os dados copiados permanecem íntegros. Você vai praticar automação com caminhos, cópia de arquivos, hashes e registro de execução usando a biblioteca padrão.

## 📝 Tarefas

### 🛠️ Criar uma cópia de backup

#### Descrição
Crie uma pasta `dados_origem` com alguns arquivos e ao menos uma subpasta. Escreva um script que copie o conteúdo para `backups`, mantendo a estrutura de pastas e criando uma nova pasta de backup identificada pela data e hora da execução.

#### Requisitos
O programa concluído deve:

- Percorrer os arquivos e subpastas de `dados_origem` usando `pathlib`.
- Copiar os arquivos com `shutil.copy2`, preservando os originais.
- Criar uma pasta de backup exclusiva para cada execução e nunca sobrescrever uma cópia anterior.

### 🛠️ Verificar a integridade dos arquivos

#### Descrição
Depois da cópia, compare cada arquivo original com sua cópia usando o algoritmo SHA-256 do módulo `hashlib`. Informe se o backup foi verificado ou se algum arquivo está ausente ou diferente.

#### Requisitos
O programa concluído deve:

- Calcular o hash de cada arquivo original e do arquivo correspondente no backup.
- Sinalizar arquivos ausentes no backup e arquivos cujo conteúdo não corresponda ao original.
- Informar claramente se todos os arquivos copiados passaram pela verificação.

### 🛠️ Registrar o resultado da execução

#### Descrição
Registre cada tentativa de backup em um arquivo de log. Inclua informações suficientes para entender quando a rotina foi executada, qual pasta foi copiada e se a verificação foi concluída com sucesso.

#### Requisitos
O programa concluído deve:

- Usar o módulo `logging` para registrar data e hora, caminhos de origem e destino e resultado da verificação.
- Registrar erros, como uma pasta de origem inexistente, sem apagar ou modificar os arquivos de origem.
- Exibir um resumo no terminal com a quantidade de arquivos copiados e o resultado final da verificação.