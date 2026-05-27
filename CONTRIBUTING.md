# 📚 Contribution Guidelines: Structure & Naming

To keep `devpapers` organized, scalable, and easy to navigate, all contributions must strictly follow the folder structure and file naming rules described below.

---

## 📂 1. Folder Structure

The repository is organized by **Area → Sub-area → Technology/Concept → Specificity → [Paper Folder]**.

Directory structure pattern:

```
[category]/[subcategory]/[technology_or_concept]/[specificity]/[paper-id-slug]
```

### Practical Example

If your paper is about memory optimization in AI agents using Neo4j, the directory tree looks like this:

```
software/
└── ia/
    └── llm/
        └── agentic/
            └── 0000000001-graph-based-cognitive-memory-otimizando-o-uso-de-tokens/
                ├── main.tex          # Main paper file
                ├── references.bib    # Bibliography (if any)
                └── imagens/          # Figures, diagrams, assets
```

---

## 🏷️ 2. Naming Conventions

### 📁 Category & Subcategory Folders

- **Always lowercase:** No uppercase letters.
- **No spaces or special characters:** Use only `a–z` and digits.
- **Separators:** Use hyphens (`-`) for multi-word categories (e.g. `computacao-em-nuvem`).

### 📦 The Paper Folder (Final Directory)

The folder containing the `.tex` file must strictly follow: `[10-digit-ID]-[title-slug]`

- **ID (Unique Identifier):** Exactly 10 digits, zero-padded (e.g. `0000000001`, `0000000002`). *Check the last ID in the repo before creating yours.*
- **Slug:** The paper title abbreviated, lowercased, without accents, and separated by hyphens.
- **Correct example:** `0000000001-graph-based-cognitive-memory-otimizando-o-uso-de-tokens`

### 📄 Internal Files

To ensure the repository is readable by automation and LaTeX build tools, internal files must use fixed names:

| File | Description | Required |
|------|-------------|----------|
| `main.tex` | Main article/paper source. | **Required** |
| `references.bib` | BibTeX bibliography file. | Optional |
| `imagens/` | Folder for figures, diagrams, and graphs. | Optional |

---

## 🛠️ 3. LaTeX Best Practices (`main.tex`)

**1. Relative paths** — When importing images, use paths relative to the paper directory:

```latex
\includegraphics{imagens/fluxograma.png}
```

**2. Encoding** — Save `main.tex` with **UTF-8** encoding.

**3. Lightweight images** — Avoid large files. Prefer optimized `.png` or vector `.pdf`.

---

## 🚀 How to Start a New Paper

1. Run `git pull origin main` to get the latest ID.
2. Identify the correct categories. If they don't exist, create them following the pattern.
3. Create your paper folder with the next available ID.
4. Add your `main.tex` and commit!

---

## 📑 Don't forget to update the Papers Index

After adding your paper, update the index table in [README.md](./README.md) with your paper's ID, title, area, author, and date.
