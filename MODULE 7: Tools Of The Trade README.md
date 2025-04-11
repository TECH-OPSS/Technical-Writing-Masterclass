# 🛠️ Module 7: Tools of the Trade

As a technical writer, your toolkit is just as important as your writing. The modern landscape of technical documentation is built on developer workflows, version control, automation, and collaborative platforms. This module introduces you to the **tools of the trade** — from lightweight markup languages to full-blown documentation platforms, AI writing assistants, and collaborative environments.

We’ll explore how to set up a docs-as-code pipeline, version your docs with Git, generate sites with tools like **MkDocs** and **Docusaurus**, and leverage AI to speed up your workflow without sacrificing quality.

---

## ✍️ **Writing Formats for Technical Documentation**

Technical documentation often lives alongside source code and is written in lightweight markup formats that are both human-readable and machine-parsable.

## Markdown (.md)

Markdown is the most widely used markup language in documentation today. It’s simple, readable, and supported by nearly every static site generator and version control platform.

**Key Features:**
- Syntax for headings, lists, links, and images
- Code blocks with language-specific highlighting
- Easy integration with GitHub, GitLab, and static site generators like MkDocs, Docusaurus

**When to use Markdown:**
- Project READMEs
- API reference docs
- Tutorials and quickstart guides

**Bold Text** and _Italic Text_

- Bullet list
1. Numbered list

```python
def hello_world():
    print("Hello, world!")
```

## reStructuredText (.rst)

Used primarily in the Python ecosystem, especially with **Sphinx**, reStructuredText is more powerful but slightly more complex than Markdown.

**Key Features:**
- Richer semantic markup
- Built-in directives (e.g., for tables of contents, figures)
- Extensible with custom roles and directives

**When to use reStructuredText:**
- Python package documentation
- Sphinx-based projects
- API and configuration docs

## AsciiDoc (.adoc)

AsciiDoc is a powerful format that can produce books, manuals, and complex tech documentation.

**Key Features:**
- Detailed formatting options
- Conditional content support
- Suitable for enterprise-level documentation

**When to use AsciiDoc:**
- Large, structured documentation sets
- Internal systems documentation
- DocBook or PDF generation

## 🌐Docs-as-Code Workflow

Docs-as-code is the practice of treating documentation like software code. This approach integrates writing into the developer workflow.

## Why Use Docs-as-Code?
- Version control with Git
- Collaboration via pull requests
- Continuous integration and deployment
- Automation and scalability

## Core Tools in a Docs-as-Code Stack:
- **Git** for version control
- **Markdown/AsciiDoc/reStructuredText** for writing
- **Static site generators** like Docusaurus or MkDocs
- **CI/CD tools** like GitHub Actions for deployment

### **Workflow Overview:**

Writer creates/updates docs → Commits changes → Opens PR → Peer review → Merge → Auto-deploys site

## 🗂️Version Control with Git & GitHub

Git and GitHub are foundational tools in the docs-as-code ecosystem. You don’t need to be a Git expert, but basic fluency is essential.

## Basic Git Commands for Writers
```bash
git clone <repo_url>
git checkout -b new-docs
git add .
git commit -m "Add getting started guide"
git push origin new-docs
```

### **Using GitHub for Documentation:**
- Open issues to track doc work
- Use pull requests for collaboration
- Leverage GitHub Actions to automate doc site builds

---

## 🚀 **Static Site Generators**

These tools turn your text files into professional documentation websites.

---

### **📘 MkDocs**

- **Format:** Markdown  
- **Target Users:** Python developers, open source projects  
- **Features:**  
  - Clean themes like Material for MkDocs  
  - Easy setup with `mkdocs.yml`  
  - Built-in search, navigation, and versioning

```bash
pip install mkdocs
mkdocs new my-project
cd my-project
mkdocs serve
```

---

### **📘 Docusaurus**

- **Format:** Markdown  
- **Target Users:** React/JavaScript developers, product teams  
- **Features:**  
  - Created by Meta  
  - Integrates React for customization  
  - Versioning and internationalization out of the box

```bash
npx create-docusaurus@latest my-site classic
cd my-site
npm start
```

---

### **📘 Sphinx**

- **Format:** reStructuredText or Markdown  
- **Target Users:** Python community, data science teams  
- **Features:**  
  - Rich extensibility with plugins  
  - API autodoc support  
  - PDF generation and LaTeX integration

```bash
pip install sphinx
sphinx-quickstart
make html
```

---

### **📘 Hugo**

- **Format:** Markdown  
- **Target Users:** Bloggers, enterprise teams  
- **Features:**  
  - Very fast builds  
  - Flexible content management  
  - Theming with Go templates

```bash
brew install hugo
hugo new site my-docs
cd my-docs
hugo server
```

---

## 🤝 **Collaboration Tools**

Docs are written by people — so collaboration is key. Here are the most commonly used tools for team-based writing.

---

### 🧠 **Notion**

- Great for internal documentation and planning
- Markdown-like editor
- Collaboration and comments built-in
- Excellent for drafting and organizing ideas

---

### 🏢 **Confluence**

- Powerful documentation tool for enterprise teams
- Page versioning and workflows
- Integrates with Jira and other Atlassian products
- Good for centralized knowledge bases

---

## 🤖 **Leveraging AI Tools for Writing and Editing**

AI is transforming the way we write, edit, and manage documentation. It won’t replace the writer, but it’s your new best assistant.

---

### ✨ **AI Writing Use Cases**
- Drafting repetitive or boilerplate text
- Summarizing complex information
- Generating code samples
- Rewriting for tone and clarity
- Translating docs

---

### ⚙️ **Popular AI Tools**
| Tool            | Use Case                                   |
|-----------------|--------------------------------------------|
| **ChatGPT**     | Drafting, rephrasing, ideation             |
| **Grammarly**   | Grammar, tone, and readability checks      |
| **GitHub Copilot** | Code sample generation and autocomplete  |
| **Quillbot**    | Paraphrasing and rewriting                 |
| **DeepL**       | Translating documentation                  |

---

### 🔍 **Best Practices for AI-assisted Writing**
- Always fact-check AI outputs
- Use AI for first drafts, not final versions
- Don’t let AI override domain-specific language
- Maintain your brand’s style guide

---

## 📚 **Real-World Scenario: End-to-End Docs Pipeline**

Imagine you’re documenting an open-source AI tool.

### ✅ Your stack might look like:

- 🖊️ Write in Markdown
- 📁 Store in GitHub
- 🔍 Review via PRs
- 🚀 Publish with MkDocs + GitHub Pages
- 🧠 Use ChatGPT to brainstorm section intros
- 🧪 Run Grammarly for polishing

---

## 💬 **Final Conclusion**

Technical writing today is deeply intertwined with the tools you use. Mastering these writing formats, static site tools, and collaboration workflows makes you far more effective and scalable. You're not just writing — you're building **living, evolving documentation systems**.

Whether you’re publishing a single README or maintaining an enterprise-level docs site, your toolkit defines the **quality**, **collaboration**, and **usability** of your work.

---
