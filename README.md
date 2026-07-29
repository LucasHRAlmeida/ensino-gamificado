# VIA - Vida Integrada e Autônoma

Plataforma educativa interativa para ensino de **Vias de Sinalização Oncológica** e os **14 Hallmarks do Câncer**. PoC para metodologia de ensino com gameficação

## 🎯 Funcionalidades

- **Exploração de Hallmarks**: Estude os 14 marcos do câncer com vias de sinalização associadas, genes-chave e fármacos direcionados
- **Quiz Interativo**: Avaliação integrada com feedback comentado e análise de desempenho
- **Importação de Dados**: Customize o conteúdo via JSON ou CSV
- **Exportação em PDF**: Gere relatórios personalizados em PDF
- **Design Responsivo**: Interface moderna e acessível em qualquer dispositivo

## 🚀 Como Usar

### Acesso Online
A aplicação está disponível via GitHub Pages:
**[Acesse aqui](https://lucashralmeida.github.io/ensino-gamificado/)**

Há também uma **versão em prosa + diagramas didáticos**: [`prosa-diagramas.html`](https://lucashralmeida.github.io/ensino-gamificado/prosa-diagramas.html)

### Executar Localmente
1. Clone o repositório:
   ```bash
   git clone https://github.com/LucasHRAlmeida/ensino-gamificado.git
   cd ensino-gamificado
   ```

2. Abra `index.html` em um navegador moderno:
   ```bash
   open index.html
   ```

## 🚀 Publicação (GitHub Pages)

O site é publicado automaticamente pelo workflow [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml), que republica o conteúdo a cada push no branch `main` (e pode ser disparado manualmente em **Actions → "Deploy to GitHub Pages" → Run workflow**).

> ⚠️ **Dependência de configuração:** para o deploy funcionar, a fonte do Pages precisa estar em **Settings → Pages → Build and deployment → Source = "GitHub Actions"**. Se essa fonte for trocada para "Deploy from a branch", **a publicação automática deixa de acontecer** e o site congela numa versão antiga. Não altere essa configuração sem necessidade.

## 📋 Estrutura

- **Hallmarks**: 14 marcos do câncer com pathways e genes-alvo
- **Quiz**: 8 questões iniciais sobre vias de sinalização
- **Casos Integradores**: Cenários clínicos para aplicação de conceitos
- **Relatórios**: Análise de desempenho com áreas para melhoramento

## 📁 Importação de Dados

### Formato JSON
Customize hallmarks, quizzes e casos através de um arquivo `JSON`:

**Template disponível**: Clique em "Baixar Template" na seção de importação

**Exemplo de estrutura:**
```json
{
  "hallmarks": [
    {
      "id": 1,
      "name": "Nome da Hallmark",
      "description": "Descrição",
      "pathways": [
        {
          "name": "Nome da Via",
          "genes": ["GENE1", "GENE2"],
          "drugs": ["Fármaco1"],
          "note": "Comentário opcional"
        }
      ]
    }
  ],
  "quizzes": [
    {
      "id": 1,
      "question": "Pergunta?",
      "options": ["A", "B", "C", "D"],
      "correct": 0,
      "hallmark": 1,
      "explanation": "Resposta comentada"
    }
  ],
  "cases": [...]
}
```

### Formato CSV (Quizzes apenas)
Importe questões rápidas com as colunas:
- `id`, `question`, `option1`, `option2`, `option3`, `option4`
- `correct` (índice: 0-3), `hallmark` (ID), `explanation`

## 🛠️ Tecnologias

- **HTML5 + CSS3 + JavaScript** (vanilla, sem dependências externas)
- **html2pdf.js** - Geração de relatórios em PDF
- **PapaParse** - Parsing de arquivos CSV
- **LocalStorage** - Persistência de dados (resultados do quiz e conteúdo customizado)

## 📝 Bugs Corrigidos

- ✅ Tratamento robusto de `localStorage` (navegadores com privacidade)
- ✅ Validação melhorada de importação CSV
- ✅ Promise handling correto em exportação de PDF
- ✅ Error handling em todas as operações críticas

## 🤖 Governança para Agentes (POP 000)

Alterações neste repositório — por agentes de IA (Claude, Grok, Copilot, etc.) ou por humanos — seguem a **[POP 000](POP-000.md)** (Procedimento Operacional Padrão).

- 📄 **Leitura obrigatória antes de qualquer alteração:** [`POP-000.md`](POP-000.md) e [`AGENTS.md`](AGENTS.md).
- 🔒 Caminhos sensíveis (workflows, `.nojekyll`, docs de governança) têm revisão de dono via [`.github/CODEOWNERS`](.github/CODEOWNERS).
- ✍️ **Todo Pull Request** deve conter, por escrito, a declaração de ter lido e seguido a POP 000 (ver [modelo de PR](.github/pull_request_template.md)).

## 👨‍🏫 Autor

**Dr Lucas HR** - Médico pela Faculdade de Medicina de Ribeirão Preto (FMRP-USP, Turma 64)

Disciplina: Biologia do Câncer - Vias de Sinalização Oncológica

## 📚 Referências

1. Hanahan D. Hallmarks of cancer: new dimensions. *Cancer Discovery*. 2022;12(1):31-46.
2. Hanahan D, Weinberg RA. Hallmarks of cancer: the next generation. *Cell*. 2011;144(5):646-674.
3. Vogelstein B, et al. Cancer genome landscapes. *Science*. 2013;339(6127):1546-1558.

## 📄 Licença

Este projeto é de domínio educacional. Sinta-se livre para adaptar, estender e compartilhar.

---

**Status**: ✅ Publicado via GitHub Pages | 🐛 Bugs corrigidos | 🚀 Pronto para uso
