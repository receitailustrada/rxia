# 🩺 RXIA — Receita Ilustrada Assistente (RAG)

![Status](https://img.shields.io/badge/Status-Ativo-success)
![Arquitetura](https://img.shields.io/badge/Arquitetura-Serverless-blue)
![Uso](https://img.shields.io/badge/Uso-Clínico%20%2F%20APS-00A651)

O **RXIA (Receita Ilustrada Assistente)** é um widget de busca com escopo estritamente fechado aos documentos oficiais do projeto (como diretrizes do INCA, protocolos do TelessaúdeRS e laudos selecionados). Publicado via GitHub Pages, ele foi desenhado para ser incorporado facilmente ao Google Sites e outras plataformas institucionais.

> **⚠️ AVISO CLÍNICO IMPORTANTE:** O RXIA responde *apenas* com base nos documentos apresentados no seu índice local (`rxi_index.json`). Ele **não substitui** a avaliação clínica. Sempre verifique os dados e a versão da fonte citada.

## 🚀 Como Usar e Incorporar
* **URL Raiz:** [https://receitailustrada.github.io/rxia/](https://receitailustrada.github.io/rxia/)
* **Widget Direto:** [https://receitailustrada.github.io/rxia/rxi_widget.html](https://receitailustrada.github.io/rxia/rxi_widget.html)
* **Integração no Google Sites:** Vá no menu `Insira` → `Incorporar` → `URL` e cole a URL do widget direto.

## 📂 Estrutura dos Arquivos
Para garantir o funcionamento em qualquer servidor estático, os seguintes arquivos devem permanecer na raiz do repositório:
- `index.html` → Realiza o redirecionamento para a interface do widget (URL curta).
- `rxi_widget.html` → A interface de busca em si (roda 100% no navegador do usuário).
- `rxi_index.json` → O índice de base de dados contendo os trechos (pedaços) e citações (título, páginas, ano, texto).

## ♻️ Como Atualizar o Índice
1. Gere um novo arquivo `rxi_index.json` incorporando seus novos PDFs (INCA, TelessaúdeRS, etc.).
2. No GitHub: Vá em **Adicionar arquivo** → **Carregar arquivos** e substitua o `.json` na raiz.
3. **Controle de Cache:** O `rxi_widget.html` busca o arquivo com um sufixo de versão (ex: `?v=20250906`). Ao atualizar o índice no futuro, edite o `rxi_widget.html` e troque esse sufixo para `?v=NOVO_NUMERO` (ex: a data da atualização) para forçar o recarregamento.

## 🛡️ Escopo, Segurança e Privacidade
* **Operação Offline/Isolada:** O widget **não consulta a web externa** para formular respostas. A busca ocorre estritamente dentro do conteúdo fornecido no `rxi_index.json`.
* **Rastreabilidade:** Cada resultado exibido acompanha uma citação direta indicando o título do documento e a página de origem.
* **Privacidade de Dados:** Exames reais (PDFs/laudos) usados como base **não devem conter dados sensíveis**. Certifique-se de realizar a anonimização rigorosa (removendo nomes, CPFs, etc.) antes da indexação.

## 📝 Licenças
* **Código deste repositório:** Licença MIT (ver arquivo `LICENSE`).
* **Conteúdo das diretrizes/laudos:** Respeite as licenças originais dos criadores (ex.: Documentos do INCA frequentemente utilizam CC BY-NC-SA).

---
*Ecossistema RXI - Ferramentas digitais para gestão clínica e saúde humanizada.*  
*📍 Cruz Alta / RS*
