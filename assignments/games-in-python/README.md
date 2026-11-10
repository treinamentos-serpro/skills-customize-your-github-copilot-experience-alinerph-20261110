
# 📘 Atividade: Jogo da Forca

## 🎯 Objetivo

Desenvolver um jogo da Forca em Python para praticar manipulação de strings, listas, condicionais, loops e entrada de dados do usuário.

## 📝 Tarefas

### 🛠️ Implementar a lógica da partida

#### Descrição
Crie a lógica principal do jogo: selecione uma palavra aleatória de uma lista predefinida e permita que o jogador tente descobri-la, uma letra por vez.

#### Requisitos
O programa concluído deve:

- Selecionar aleatoriamente uma palavra de uma lista predefinida.
- Exibir cada letra ainda não descoberta como um sublinhado, mantendo visíveis as letras acertadas.
- Registrar cada palpite e reduzir o número de tentativas restantes quando a letra não estiver na palavra.
- Encerrar a partida quando a palavra for descoberta ou quando as tentativas restantes chegarem a zero.

### 🛠️ Tratar palpites e concluir a partida

#### Descrição
Complete a interação com o jogador, validando os palpites e informando claramente o resultado da partida.

#### Requisitos
O programa concluído deve:

- Aceitar um palpite de uma única letra por vez.
- Rejeitar entradas vazias, com mais de um caractere ou que não sejam letras, sem consumir uma tentativa.
- Informar quando o jogador venceu ou perdeu e, em caso de derrota, revelar a palavra escolhida.