RXIA — Receita Ilustrada Assistente (RAG com solicitações)
RXIA é um widget de busca com escopo fechado aos documentos oficiais do projeto (diretrizes INCA, TelessaúdeRS e laudos selecionados).
Ele é publicado no GitHub Pages e pode ser incorporado ao Google Sites .

⚠️ Aviso : O RXIA responde apenas com base nos documentos apresentados no índice ( rxi_index.json).
Não substitui avaliação clínica. Sempre verifique os dados/versão da fonte.

✅ Como usar (resumo)
URL raiz:https://receitailustrada.github.io/rxia/
Widget direto:https://receitailustrada.github.io/rxia/rxi_widget.html
No Google Sites : Insira → Incorporar → URL e cole a URL do widget.

📁 Estrutura dos arquivos
index.html→redirecionamento para o widget (URL curta).
rxi_widget.html→ interface de busca (roda 100% sem navegador).
rxi_index.json→ índice com trechos (pedaços) e citações (título, páginas, ano, texto).
Os arquivos acima devem ficar na raiz do repositório.

♻️ Atualizar o índice ( rxi_index.json)
Gere um novo rxi_index.jsoncom seus PDFs (INCA, TelessaúdeRS, etc.).
No GitHub: Adicionar arquivo → Carregar arquivos e substituir o arquivo na raiz.
Para evitar cache do navegador, o rxi_widget.htmljá busca com sufixo ?v=20250906.
Quando atualizar o índice novamente no futuro, edite o rxi_widget.htmle troque o sufixo para ?v=NOVO_NUMERO.
🛡️ Escopo e segurança
Sem internet/externo: o widget não consulta a web ; busca apenas no rxi_index.json.
Cada resultado vem com citação : título + páginas.
Exames reais (PDFs/laudos) não devem conter dados sensíveis. Se existirem, anonimize antes de indexar.
🧩 Incorporar em outras páginas
Basta hospedar rxi_widget.htmle rxi_index.jsonreunir em qualquer servidor estático (ou outro repositório de páginas).

📝 Licenças
Código deste repositório: MIT (ver LICENSE).
Conteúdo das diretrizes/laudos: respeite as licenças originais (ex.: INCA — CC BY‑NC‑SA).
📮 Contato
Receita Ilustrada — RXI (Cruz Alta/RS)
Atualizado em: 06/09/2025
