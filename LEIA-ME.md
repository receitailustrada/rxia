# RXIA — Receita Ilustrada Assistente (RAG com citações)

**RXIA** é um widget de busca **com escopo fechado** aos documentos oficiais do projeto (diretrizes INCA, TelessaúdeRS e laudos selecionados).  
Ele publica no **GitHub Pages** e pode ser incorporado ao **Google Sites**.

> ⚠️ **Aviso**: O RXIA responde apenas com base nos documentos presentes no índice (`rxi_index.json`).  
> Não substitui avaliação clínica. Sempre verifique data/versão da fonte.

## ✅ Como usar (resumo)
- URL raiz: `https://receitailustrada.github.io/rxia/`
- Widget direto: `https://receitailustrada.github.io/rxia/rxi_widget.html`

No **Google Sites**: *Inserir → Incorporar → URL* e cole a URL do widget.

---

## 📁 Estrutura dos arquivos
- `index.html` → redireciona para o widget (URL curta).
- `rxi_widget.html` → interface de busca (roda 100% no navegador).
- `rxi_index.json` → **índice** com trechos (chunks) e **citações** (título, páginas, ano, texto).

> Os arquivos acima devem ficar **na raiz** do repositório.

---

## ♻️ Atualizar o índice (`rxi_index.json`)
1. Gere um novo `rxi_index.json` com seus PDFs (INCA, TelessaúdeRS, etc.).  
2. No GitHub: **Add file → Upload files** e substitua o arquivo na raiz.  
3. Para evitar cache do navegador, o `rxi_widget.html` já busca com sufixo `?v=20250906`.  
   - Quando atualizar o índice novamente no futuro, edite o `rxi_widget.html` e troque o sufixo para `?v=NOVO_NUMERO`.

---

## 🛡️ Escopo e segurança
- Sem internet/externo: o widget **não consulta a web**; busca apenas no `rxi_index.json`.
- Cada resultado vem com **citação**: título + páginas.
- Exames reais (PDFs/laudos) não devem conter dados sensíveis. Se existirem, **anonimize** antes de indexar.

---

## 🧩 Incorporar em outras páginas
Basta hospedar `rxi_widget.html` e `rxi_index.json` juntos em qualquer servidor estático (ou outro repositório Pages).

---

## 📝 Licenças
- **Código** deste repositório: MIT (ver `LICENSE`).  
- **Conteúdo** das diretrizes/laudos: respeite as licenças originais (ex.: INCA — CC BY‑NC‑SA).

---

## 📮 Contato
Receita Ilustrada — RXI (Cruz Alta/RS)  
Atualizado em: 2025-09-06
