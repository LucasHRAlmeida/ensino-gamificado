# VIA - Vida Integrada e Autônoma

Plataforma educativa interativa para ensino de **Vias de Sinalização Oncológica** e os **14 Hallmarks do Câncer**.

## 🎯 Funcionalidades

- **Exploração de Hallmarks**: Estude os 14 marcos do câncer com vias de sinalização associadas, genes-chave e fármacos direcionados
- **Quiz Interativo**: Avaliação integrada com feedback comentado e análise de desempenho
- **Importação de Dados**: Customize o conteúdo via JSON ou CSV
- **Exportação em PDF**: Gere relatórios personalizados em PDF
- **Design Responsivo**: Interface moderna e acessível em qualquer dispositivo

## 🚀 Como Usar

### Acesso Online
A aplicação está disponível via GitHub Pages:
**[Acesse aqui](https://lucashralmeid.github.io/ensino-gamificado/)**

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
- **LocalStorage** - Persistência de dados de sessão

## 📝 Bugs Corrigidos

- ✅ Tratamento robusto de `localStorage` (navegadores com privacidade)
- ✅ Validação melhorada de importação CSV
- ✅ Promise handling correto em exportação de PDF
- ✅ Error handling em todas as operações críticas

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
