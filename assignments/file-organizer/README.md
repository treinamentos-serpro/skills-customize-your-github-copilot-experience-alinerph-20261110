# 📘 Assignment: Organizador de Arquivos

## 🎯 Objective

Crie um script simples para organizar arquivos por extensão. Você vai praticar caminhos de arquivos, repetição e automação usando uma pasta de teste, mantendo os arquivos originais intactos.

## 📝 Tasks

### 🛠️ Explorar os arquivos de entrada

#### Descrição
Crie uma pasta chamada `arquivos_entrada` com alguns arquivos de tipos diferentes, como `agenda.txt`, `foto.jpg`, `dados.csv` e `sem_extensao`. Use `pathlib` para percorrer os arquivos e identificar a extensão de cada um.

#### Requisitos
O programa concluído deve:

- Percorrer os arquivos diretamente dentro de `arquivos_entrada`.
- Exibir o nome e a extensão de cada arquivo.
- Identificar arquivos sem extensão e agrupá-los com o nome `sem_extensao`.

### 🛠️ Preparar as pastas de destino

#### Descrição
Com base nas extensões encontradas, crie uma pasta `arquivos_organizados` e uma subpasta para cada tipo de arquivo. Por exemplo, arquivos `.txt` devem ficar destinados à pasta `txt`.

#### Requisitos
O programa concluído deve:

- Criar `arquivos_organizados` caso ela ainda não exista.
- Criar uma subpasta para cada extensão presente em `arquivos_entrada`.
- Usar a pasta `sem_extensao` para arquivos sem extensão.

### 🛠️ Copiar os arquivos para suas categorias

#### Descrição
Complete o organizador copiando cada arquivo da pasta de entrada para a subpasta correspondente. Use `shutil.copy2` para preservar os originais e permitir executar o script novamente.

#### Requisitos
O programa concluído deve:

- Copiar cada arquivo para a pasta correspondente à sua extensão.
- Deixar todos os arquivos originais em `arquivos_entrada`.
- Exibir uma mensagem ao terminar, informando onde os arquivos organizados foram salvos.
