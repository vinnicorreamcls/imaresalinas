# Imaré Salinas — versão trilíngue (PT · EN · ES)

## Como instalar
Copie o conteúdo deste zip para a raiz do site, ao lado da pasta `assets/` (que não foi enviada e não precisa ser duplicada):

    /index.html, /suitebrisa.html, ...   -> português (mesmos arquivos de antes + seletor de idioma e hreflang)
    /en/index.html, /en/suitebrisa.html  -> inglês
    /es/index.html, /es/suitebrisa.html  -> espanhol
    /assets/...                          -> suas imagens e vídeos (inalterados)

As páginas em /en/ e /es/ buscam imagens em `../assets/`. Se o servidor já atende `/suitebrisa` sem ".html",
ele também deve atender `/en/suitebrisa` e `/es/suitebrisa` da mesma forma.

## Decisões tomadas
- A página inicial (EN e ES) agora é gerada a partir do `index.html` atual em português (com Como chegar, Transporte,
  Parceiros, galerias dos espaços compartilhados, clima OpenWeather e horário de silêncio 22h–08h). As versões
  anteriores de `/en/index.html` e `/es/index.html`, baseadas no `index-atualizado.html`, foram substituídas.
  O `index.html` em português recebeu o seletor de idioma (PT · EN · ES) e as tags hreflang, como as demais páginas.
- Mensagens pré-preenchidas do WhatsApp nos cartões das suítes foram traduzidas no index em EN e ES.
- Nomes próprios mantidos: Imaré Salinas, Casa Duna, nomes das suítes, praias e lugares (EN: "Atalaia Beach"; ES: "Praia do Atalaia").
- "Pousada" = "guesthouse" (EN) / "posada" (ES). Horários em formato 12h no inglês.
- Textos dentro dos scripts também foram traduzidos (galerias, tábua de marés, clima). Dias e meses da tábua usam o idioma da página.
- sitemap.xml e llms.txt atualizados com as três versões e `hreflang`.

## Pontos para revisar
1. Textos em primeira pessoa na página Cultura ("Não encontrei confirmação de bilheteria…"). Parecem anotações de pesquisa; vale reescrever em português e retraduzir.
2. Horário de silêncio: o index atual usa 22h–08h; as páginas das suítes podem ter outro horário. Confirme qual vale.
3. A chave da API do OpenWeather está escrita no código de `index.html` e `pontosturisticos.html` (visível a qualquer visitante). Restrinja-a ao seu domínio no painel do OpenWeather ou troque por uma chave nova.
4. A tábua de marés offline cobre apenas 2026. A partir de 2027 o plano B da página (quando a API não responde) deixa de funcionar.
5. Revisão por falante nativo recomendada para textos comerciais e regras da casa.
