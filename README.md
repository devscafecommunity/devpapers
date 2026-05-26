# 📚 Diretrizes de Contribuição: Estrutura e Nomenclatura

Para manter o `devpapers` organizado, escalável e fácil de navegar, todas as contribuições devem seguir estritamente as regras de estruturação de pastas e nomenclatura de arquivos descritas abaixo.

---

## 📂 1. Estrutura de Pastas (Arquitetura)

O repositório é organizado por **Área > Subárea > Tecnologia/Conceito > Especificidade > [Pasta do Paper]**.

A estrutura de diretórios deve seguir o padrão:
```text
[categoria]/[subcategoria]/[tecnologia_ou_conceito]/[especificidade]/[id_slug_do_paper]

```

### Exemplo Prático:

Se o seu paper fala sobre otimização de memória em agentes de IA usando Neo4j, a árvore de diretórios ficará assim:

```text
software/
└── ia/
    └── llm/
        └── agentic/
            └── 0000000001-graph-based-cognitive-memory-otimizando-o-uso-de-tokens/
                ├── main.tex          # Arquivo principal do paper
                ├── referencias.bib   # Fontes e citações (se houver)
                └── imagens/          # Gráficos, diagramas e assets

```

---

## 🏷️ 2. Regras de Nomenclatura (Naming Conventions)

### 📁 Pastas de Categorias e Subcategorias

* **Sempre em caixa baixa (lowercase):** Não utilize letras maiúsculas.
* **Sem espaços ou caracteres especiais:** Use apenas letras de `a` a `z` e números.
* **Separadores:** Use hifens (`-`) se uma categoria precisar de mais de uma palavra (ex: `computacao-em-nuvem`).

### 📦 A Pasta do Paper (O Diretório Final)

A pasta que contém o arquivo `.tex` deve seguir rigidamente o formato: `[ID de 10 dígitos]-[slug-do-titulo-em-ingles-ou-portugues]`

* **ID (Identificador Único):** Deve conter exatamente 10 dígitos, completados com zeros à esquerda (ex: `0000000001`, `0000000002`). *Verifique o último ID do repositório antes de criar o seu.*
* **Slug:** O título do paper resumido, convertido para caixa baixa, sem acentos e separado por hifens.
* **Exemplo Correto:** `0000000001-graph-based-cognitive-memory-otimizando-o-uso-de-tokens`

### 📄 Arquivos Internos

Para garantir que o repositório seja legível por ferramentas de automação e compilação de LaTeX, os arquivos internos devem ter nomes fixos:

| Arquivo | Descrição | Obrigatoriedade |
| --- | --- | --- |
| `main.tex` | Arquivo principal do artigo/paper. | **Obrigatório** |
| `references.bib` | Arquivo de referências bibliográficas do BibTeX. | Opcional |
| `imagens/` | Pasta para armazenar figuras, diagramas e gráficos. | Opcional |

---

## 🛠️ 3. Boas Práticas para o LaTeX (`main.tex`)

1. **Caminhos Relativos:** Ao importar imagens, use caminhos relativos ao diretório do paper.
```latex
\includegraphics{imagens/fluxograma.png}

```


2. **Encoding:** Certifique-se de salvar o arquivo `main.tex` com a codificação **UTF-8**.
3. **Imagens Leves:** Evite subir imagens pesadas (formatos `.png` otimizados ou `.pdf` vetoriais são preferíveis).

---

## 🚀 Como começar um novo Paper?

1. Dê um `git pull origin main` para garantir que pegou o último ID gerado.
2. Identifique as categorias corretas. Se não existirem, crie-as seguindo o padrão.
3. Crie a pasta do seu paper com o próximo ID disponível.
4. Adicione seu `main.tex` e faça o commit!
