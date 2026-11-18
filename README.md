# Portfólio acadêmico — Keity Suelyn Giasson Da Silva

## Publicação
Envie os arquivos desta pasta para a raiz do repositório `keitygiasson/portfolio-academico`. Em Settings > Pages, selecione a publicação via GitHub Actions com HTML estático ou branch main / (root).

## Recursos disponíveis sem cadastro adicional
O dashboard, a projeção exploratória, as perguntas livres em modo local e a busca da wiki funcionam no navegador. **O assistente local não é um LLM** e não deve ser apresentado como tal. O relatório PDF e os slides estão incluídos.

## Opcional: conectar uma IA generativa com plano gratuito
A disponibilidade, os limites e as condições do plano gratuito do provedor podem mudar. O uso gratuito não é garantido.
1. Crie uma chave no Google AI Studio e confira os termos e cotas aplicáveis. Não publique a chave no GitHub.
2. Crie um Cloudflare Worker e cole o conteúdo de `worker.js`.
3. Em Worker > Settings > Variables and Secrets, crie `GEMINI_API_KEY` como **Secret**; opcionalmente `ALLOWED_ORIGIN` com `https://keitygiasson.github.io` e `GEMINI_MODEL` conforme modelo disponível na sua conta.
4. Publique o Worker. Copie a URL HTTPS do Worker.
5. No `index.html`, encontre `const CONFIG={endpoint:''}` e coloque a URL do Worker entre as aspas; envie a versão atualizada ao GitHub.
6. Teste perguntas livres no site. A chave continua no servidor, não no navegador.

**Segurança:** esse Worker de demonstração confere a origem, mas a origem HTTP não autentica usuários e pode ser simulada. Para publicação com tráfego elevado, implemente rate limiting, proteção contra abuso e monitoramento de cotas. Não armazene dados sensíveis.

## Limitações metodológicas
Os dados vão de 2025-01-01 a 2026-08-03. Agosto/2026 é parcial. A previsão é uma regressão linear exploratória sobre meses completos, sem validação fora da amostra ou ajuste de sazonalidade. Receita não equivale a lucro.
