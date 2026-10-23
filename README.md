# 🧩 Missão Conjuntos

> Aprenda teoria dos conjuntos por meio de desafios interativos, diagramas de Venn e missões educativas.

![Godot](https://img.shields.io/badge/Godot-4.4.1-478CBF?logo=godotengine&logoColor=white)
![GDScript](https://img.shields.io/badge/Linguagem-GDScript-355570)
![Categoria](https://img.shields.io/badge/Categoria-Jogo%20Educacional-2EA44F)

## 📖 Sobre o projeto

**Missão Conjuntos** é um jogo educacional desenvolvido em Godot para apoiar o aprendizado de matemática de alunos do ensino médio.

O jogador resolve desafios sobre **definição de conjuntos, união, interseção, complemento e subconjuntos**, recebendo dicas e explicações durante as atividades.

## 🎯 Objetivo

Tornar o estudo de conjuntos mais acessível e interativo, permitindo que o jogador pratique conceitos matemáticos e acompanhe seu progresso.

## 🚀 Enredo

Uma tempestade danificou os arquivos da nave **Atlas**.

Para reconstruir o mapa e reativar o portal de retorno, a exploradora **Lia** precisa restaurar cinco setores. Cada setor representa um conceito matemático, e o jogador deve completar as missões para recuperar os sistemas da nave.

## 🎮 Modos de jogo

### Missões interativas

O jogador seleciona elementos ou conjuntos de acordo com o objetivo apresentado.

- **Cinco setores temáticos.**
- **30 desafios disponíveis**, sendo seis por tema.
- **Três desafios sorteados** por missão.
- Novas tentativas após respostas incorretas.
- Dicas e feedback explicativo.

### Avaliação final

Uma avaliação reúne questões dos cinco temas estudados.

- Banco com **15 questões**.
- **Dez questões sorteadas** por partida, duas de cada tema.
- Uma alternativa correta por questão.
- Correção comentada após cada resposta.
- Registro do melhor resultado.

## 📚 Conteúdos abordados

| Setor | Conteúdo | Atividade |
|---|---|---|
| O arquivo perdido | Definição e pertinência | Identificar elementos de uma coleção |
| Pontes de união | União — A ∪ B | Reunir elementos dos dois conjuntos |
| O núcleo comum | Interseção — A ∩ B | Encontrar elementos compartilhados |
| Além da fronteira | Complemento em U | Identificar elementos de U que não pertencem a A |
| Coleções dentro de coleções | Subconjuntos — C ⊆ A | Reconhecer conjuntos inteiramente contidos em A |

Também são trabalhados o **conjunto vazio**, a **ausência de repetição de elementos** e a importância do **universo** no cálculo do complemento.

## ✨ Funcionalidades

- ✅ Interface em português.
- ✅ Tutorial com instruções.
- ✅ Explicações e exemplos antes das missões.
- ✅ Sorteio de desafios e questões.
- ✅ Diagramas de Venn nas atividades de união e interseção.
- ✅ Feedback visual e sonoro.
- ✅ Dicas durante as atividades.
- ✅ Sistema de pontuação e estrelas.
- ✅ Salvamento local do progresso.
- ✅ Opção de ativar ou desativar o áudio.
- ✅ Navegação por mouse ou teclado.

## 🕹️ Controles

| Ação | Comando |
|---|---|
| Selecionar ou desmarcar uma opção | Clique do mouse |
| Navegar entre controles | `Tab` |
| Voltar ao controle anterior | `Shift + Tab` |
| Acionar um botão selecionado | `Espaço` ou `Enter` |

> **Conjunto vazio:** nas missões, deixe todos os itens desmarcados e confirme para indicar uma resposta vazia.

> **Subconjuntos:** cada opção representa um conjunto inteiro.

## ⭐ Pontuação

### Pontos por desafio

| Resultado | Pontos |
|---|---:|
| Acerto na primeira tentativa | 100 |
| Acerto após um erro | 75 |
| Acerto após dois ou mais erros | 50 |

### Estrelas por missão

| Conquista | Recompensa |
|---|---|
| Concluir os três desafios | ⭐ |
| Alcançar pelo menos 225 pontos | ⭐⭐ |
| Alcançar 300 pontos | ⭐⭐⭐ |

Na avaliação final, cada resposta correta vale **um ponto**, com resultado máximo de **10 pontos**.

Consultar dicas não reduz a pontuação.

## 🛠️ Tecnologias

| Tecnologia | Aplicação |
|---|---|
| Godot 4.4.1 Standard | Motor do jogo e interface |
| GDScript | Lógica, navegação, pontuação e salvamento |
| JSON | Armazenamento dos desafios e gabaritos |
| WAV | Efeitos sonoros |
| Python | Validação independente dos gabaritos |

> Python é utilizado nos testes e não é necessário para jogar.

## 📂 Organização do projeto

| Arquivo ou pasta | Responsabilidade |
|---|---|
| `project.godot` | Configurações do projeto |
| `main.tscn` | Cena principal |
| `scripts/main.gd` | Telas, sorteio, seleção, pontuação e progresso |
| `scripts/venn.gd` | Desenho dos diagramas de Venn |
| `assets/data.json` | Atividades e gabaritos |
| `assets/` | Recursos de áudio e dados |
| `tests/integration.gd` | Testes de integração |
| `tests/validate_math.py` | Validação matemática |
| `export_presets.cfg` | Configurações de exportação |

A interface é construída por código durante a execução.

## ▶️ Como executar

### Pelo Godot

1. Instale o **Godot 4.4.1 Standard**.
2. Extraia a pasta do projeto.
3. Abra o Godot e selecione **Importar**.
4. Escolha o arquivo `project.godot`.
5. Aguarde a importação dos recursos.
6. Pressione **F5** para iniciar.

> O projeto utiliza Godot 4 e não é compatível com Godot 3.

### Pelo executável Windows

1. Extraia o pacote Windows.
2. Abra `MissaoConjuntos.exe`.

Não é necessário instalar o Godot para executar essa versão.

### Pelo navegador

A exportação Web precisa ser disponibilizada por um servidor HTTP ou HTTPS.

Para testar localmente com Python instalado, execute na pasta da exportação:

```bash
python -m http.server 8000
```

Depois, acesse:

```text
http://localhost:8000
```

Mantenha todos os arquivos exportados na mesma pasta.

## 💾 Salvamento

O jogo salva localmente:

- As melhores estrelas de cada setor.
- O recorde da avaliação final.
- A preferência de áudio.

Os dados ficam armazenados em:

```text
user://progress.cfg
```

Ao retornar ao início, a missão em andamento é encerrada. Apenas resultados concluídos ficam registrados.

## 🧪 Testes e validação

- **142 verificações de integração** no Godot.
- Validação independente dos gabaritos dos 30 desafios.
- Revisão das respostas das 15 questões.
- Revisão visual das principais telas.
- Exportação para Windows e Web.

Para executar os testes a partir da pasta do projeto:

```bash
godot --headless --path . --script res://tests/integration.gd
python3 tests/validate_math.py
```

> Os testes de integração podem alterar o progresso local. Após executá-los, apague o progresso pelo menu, se necessário.

O executável Windows foi exportado, mas não foi executado em um sistema Windows no ambiente de desenvolvimento utilizado.

## 🎓 Contexto acadêmico

Ao concluir os cinco setores, o jogador realiza **15 desafios matemáticos**, além das questões da avaliação final.

O projeto pode ser utilizado em atividades de sala de aula, apresentações acadêmicas e práticas de revisão de teoria dos conjuntos.

A apresentação em slides, a publicação de uma forma de acesso ao jogo e os testes de usabilidade com participantes reais devem ser realizados pela equipe.
