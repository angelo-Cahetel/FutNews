# FutNews

## APIs que podem ser utilizadas
1. Bucar informações de partidas com [API futebol](https://www.api-futebol.com.br/)
2. Buscar tweets com [API do X](https://developer.x.com/en/docs/x-api)
3. Buscar artigos de notícias [NewsAPI](NewsAPI.org)

## Fluxo

O fluxo seria assim:
1. Usuário acessa o site e escolhe o time, exemplo: "Grêmio"
2. Front envia pedido `GET /noticias?time=gremio`
3. Back recebe o pedido e:
   - chama API de noticas e pesquisa pelo time
   - chama a API futebol e busca a tabela e próximo jogo
   - chama a API do Twitter
4. Junta tudo em uma lista e retorna para o front
5. Front exibe a lista

## Como visualizar os Tweets

### 1ª opção (linha do tempo)
- o que é: um widget que mostra os tweets mais recentes de uma conta específica
- prós: fácil implementação. não precisa de chaves de API ou backend para isso
- contras: limitado. só pode mostrar uma conta, lista ou hastag específica, não pode misturar resultads
- link da implementação: https://publish.twitter.com/

### 2ª opção (api do X)
- prós: controle total. Pode buscar por `#gremio` ou "Noticias do Grêmio" e receber os tweets em formato `JSON`, podendo formatar como a gente quiser
- contras: o plano gratuito é limitado. talvez não permita a busca
