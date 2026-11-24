# JBA Placar — publicação no GitHub Pages

Projeto estático feito com HTML, CSS e JavaScript puro. Não precisa de backend, banco de dados ou etapa de build.

## Publicar

1. Crie um repositório no GitHub (ex.: `jba-placar`). Para GitHub Free, deixe o repositório público.
2. Envie **todos os arquivos desta pasta para a raiz do repositório**. O `index.html` deve ficar na raiz, ao lado de `app.js`, `style.css`, `display.html`, `display.js` e `display.css`.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/(root)`, depois clique em **Save**.
6. Aguarde a publicação e abra o endereço mostrado em **Settings → Pages**. Em geral, será `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Como usar

- Abra o endereço publicado para acessar a mesa de controle.
- Use o botão **Abrir telão** para abrir `display.html` em outra aba/janela.
- Para sincronização, mesa e telão devem estar no mesmo navegador e computador.

## Limitação importante

O placar salva os dados no `localStorage` do navegador e sincroniza as duas telas usando `BroadcastChannel`. Portanto, publicar no GitHub Pages disponibiliza o site pela internet, mas **não sincroniza a partida entre computadores ou celulares diferentes**. Para isso, será necessário adicionar um serviço de backend/banco de dados ou uma camada de tempo real.

Os dados da partida não são enviados ao GitHub; ficam no navegador utilizado. Exporte o backup JSON após a partida.


## Configuração JBA atualizada
- Cada quarto: **12 minutos**.
- Relógio de posse padrão: **30 segundos**.
- Reinício alternativo do relógio de posse: **15 segundos**.
- Prorrogação permanece em 5 minutos.

Substitua os arquivos antigos no GitHub pelos arquivos desta versão e faça um novo commit. A aplicação migra automaticamente o padrão antigo salvo no navegador (10:00/24s) para 12:00/30s.
