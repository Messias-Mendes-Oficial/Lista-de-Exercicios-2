# Lista 2: Noções de Grafos (Parte 2) — Conceitos Básicos

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Messias-Mendes-Oficial/Lista-de-Exercicios-2/blob/main/codigo/Lista_2_Teoria_dos_Grafos.ipynb)

📄 **Documentação e Relatórios**

* [Ver Código Completo e Execução no Google Colab](https://colab.research.google.com/github/Messias-Mendes-Oficial/Lista-de-Exercicios-2/blob/main/codigo/Lista_2_Teoria_dos_Grafos.ipynb)
* [Diário de Bordo — Uso de IA](./Di%C3%A1rio%20de%20Bordo%20%E2%80%94%20Uso%20de%20IA)
* [Respostas Manuscritas / Digitalizadas (`respostas/`)](./respostas)
* [ Figuras e Gráficos Gerados (`prints/`)](./prints)

Este repositório contém a resolução da **Lista de Exercícios 2** da disciplina de **Teoria dos Grafos** (3º Período — 2026/2), ministrada pelo **Prof. Newarney T. Costa** no **Instituto Federal Goiano — Campus Iporá** (Bacharelado em Ciência da Computação).

O objetivo principal deste trabalho é consolidar e verificar computacionalmente os conceitos fundamentais de Teoria dos Grafos — incluindo representações matriciais ($A$, $B$, $A^2$, $B \cdot B^T$, $B^T \cdot B$), listas de adjacência não simétricas, grafos complementares e grafos-universo, Lema do Aperto de Mãos, graus e semigraus ($d^+, d^-$), grafos bipartidos, isomorfismo, classificação de percursos (cadeia, ciclo, circuito, simples e elementar), cliques, realizabilidade de sequências de graus, conexidade em dígrafos ($s$-conexo, $sf$-conexo e $f$-conexo), **Algoritmo de Malgrange** para componentes fortemente conexas, conectividade vértice $k(G)$ e **grafos antirregulares**. Todos os códigos foram estruturados para execução direta no **Google Colab**.

## 👥 Integrantes

* **Messias Junio da Silva Mendes** (Messias-Mendes-Oficial) | **Bruno Alves Mendonça De Abreu Filho**

## 🛠️ Tecnologias Utilizadas

* **Python 3** ( Linguagem base para modelagem algébrica e verificação dos grafos )
* **Google Colab** ( Ambiente de execução interativo em nuvem para os notebooks `.ipynb` )
* **NetworkX** ( Construção, análise de isomorfismo, bipartição, conexidade e conectividade $k(G)$ )
* **NumPy** ( Operações matriciais para cálculo de $A^2$, $B \cdot B^T$ e $B^T \cdot B$ )
* **Matplotlib** ( Visualização e exportação das figuras dos grafos para a pasta `prints/` )

## 📂 Estrutura do Repositório

| Caminho / Arquivo | Descrição |
| :--- | :--- |
| `codigo/Lista_2_Teoria_dos_Grafos.ipynb` | Notebook principal configurado para rodar 100% no **Google Colab**, contendo a resolução e validação computacional das 16 questões. |
| `prints/` | Imagens e diagramas gerados pelo notebook no Colab ilustrando os grafos das questões. |
| `respostas/` | Arquivos PDF / fotos legíveis das respostas manuscritas ou digitadas com o nome dos dois integrantes. |
| `Diário de Bordo — Uso de IA` | Registro detalhado por sessão do processo de estudo com IA e reflexão final (~½ página), conforme modelo exigido na lista. |
| `LICENSE` | Licença MIT do repositório. |
| `README.md` | Documentação geral e guia de execução do projeto. |

## 📋 Resumo das Questões Abordadas no Colab

| Questão | Tópico Principal | Implementação e Verificação no Colab |
| :--- | :--- | :--- |
| **Questão 1** | Representações e grau via matriz | Lista de adjacência, matriz de adjacência $A$, matriz de incidência $B$ e interpretação algébrica e combinatória de $A^2$, $B \cdot B^T$ e $B^T \cdot B$. |
| **Questão 2** | Listas de adjacência não simétricas | Conversão de lista simétrica ($2m = 16$ entradas) para lista não simétrica ($m = 8$ entradas) economizando índices. |
| **Questão 3** | Grafo completo / universo e complementar | Construção de $G$, $\overline{G}$ e grafo-universo não orientado ($K_n$ com $n(n-1)/2$ arestas) e orientado ($n(n-1)$ arcos sem laços / $n^2$ com laços). |
| **Questão 4** | Grau e Lema do Aperto de Mãos | Demonstração formal de $\sum_{v \in V} d(v) = 2m$ e paridade do número de vértices de grau ímpar, com validação empírica. |
| **Questão 5** | Graus e semigraus ($d^+, d^-$) | Cálculo automatizado de $d(v)$ no grafo não orientado e $d^+(v), d^-(v), d(v)$ no grafo orientado da figura. |
| **Questão 6** | Grafo bipartido e isomorfismo | Prova da ausência de ciclos ímpares (Teorema de König) e teste de bipartição mostrando que o Grafo 1 possui ciclo $C_5$ (não bipartido) enquanto o Grafo 2 ($Q_3$) é bipartido. |
| **Questão 7** | Percursos: cadeia, ciclo, circuito | Classificação dos percursos realçados em $G_1$ a $G_7$ (simples, elementar, fechado, ciclo e circuito). |
| **Questão 8** | Clique, complementar e bipartido completo | Identificação do clique $K_4$, relação entre clique em $G$ e conjunto independente em $\overline{G}$, e complementar de $K_{p,q}$. |
| **Questão 9** | Isomorfismo em grafos $(n=5)$ | Construção dos 2 grafos não isomorfos com $n=5, m=8$ (via complementares de 2 arestas) e enumeração dos 4 grafos não isomorfos com $n=5, m=7$. |
| **Questão 10** | Sequência de graus (realizabilidade) | Prova de impossibilidade da sequência $(9, 7, 6, 4, 3, 3, 3, 1, 1, 1)$ via contagem de adjacências e algoritmo de Havel-Hakimi. |
| **Questão 11** | Grafo regular e paridade | Demonstração da inexistência de grafos $(2k-1)$-regulares com $2r-1$ vértices via Lema do Aperto de Mãos. |
| **Questão 12** | Conexidade em grafos orientados | Construção e plotagem de dígrafos não conexo, $s$-conexo, $sf$-conexo e $f$-conexo. |
| **Questão 13** | Caminho em grafos $sf$-conexos e $f$-conexos | Demonstração por indução/ordenação topológica de componentes fortemente conexas da existência de passeio dirigido abrangente. |
| **Questão 14** | Componentes fortemente conexas (Malgrange) | Explicação e execução passo a passo do **Algoritmo de Malgrange** ($\Gamma^+(v) \cap \Gamma^-(v)$) em um grafo orientado inédito. |
| **Questão 15** | Conectividade $k(G)$ por inspeção | Determinação de $\kappa(G)$ e cortes mínimos de vértices para os três grafos da figura ($\kappa = 2, 2, 4$). |
| **Questão 16** | Sequência de graus e grafo antirregular | Análise da quantidade máxima de graus distintos ($n-1$), propriedades da sequência de graus e construção explícita para $n=8$ e $n=9$. |

## 🚀 Como Executar no Google Colab

1. Clique no botão **Open in Colab** no topo deste `README.md` (ou acesse diretamente o arquivo `codigo/Lista_2_Teoria_dos_Grafos.ipynb`).
2. No menu superior do Google Colab, selecione **Ambiente de execução > Executar tudo** (`Ctrl + F9`).
3. Todas as bibliotecas utilizadas (`numpy`, `networkx`, `matplotlib`) já vêm pré-instaladas por padrão no Google Colab, garantindo execução imediata sem necessidade de configuração adicional.
