# La maketa de la Míriam · v3

Web per a mòbil, en català. Publica la carpeta SENCERA (Cloudflare Pages, Netlify, GitHub Pages).

## 1. La cançó: «Vino tinto»
En obrir-se la targeta (la revelació d'ESTOPA) s'incrusta el **videoclip oficial** (canal EstopaVEVO, YouTube) en un marc de paper i arrenca sol. Quan sona, la música instrumental s'apaga i, en acabar el fragment, torna.
- Ajusta el fragment a `FINAL_MUSIC` (a l'inici del `<script>` d'index.html): `start` i `end` en segons. Ara és 0:44–1:14, **una estimació**: escolta el vídeo i posa `start` al començament del cor.
- **Només funciona amb la web publicada en https i amb internet** (comprovat: des d'una pàgina https el vídeo carrega i arrenca sol; des d'un fitxer local, no). Obrint index.html com a fitxer o en una vista prèvia YouTube dona «Error 153»; per això la web no mostra el vídeo en aquest cas (i si YouTube falla, l'amaga) i continua la música original.
- A l'iPhone el navegador pot bloquejar el so automàtic dins d'un vídeo incrustat: si passa, el vídeo es veu al marc i ella pot tocar el play del mateix YouTube. La música original continua mentrestant.
- Alternativa sense internet: un MP3 teu a `audio/estopa.mp3` i escriure `src:'audio/estopa.mp3'` (té prioritat sobre YouTube). Fes-lo servir només en privat.

## 2. Personalitza (bloc `GIFT`, també a l'inici del `<script>`)
- `letter`: la carta. **Escriu-hi un record vostre de veritat**; el text per defecte és genèric.
- `sale`: venda general anunciada per la banda: 17 nov 2026, 22:22. Comprova-ho a la venda oficial abans d'enviar-ho.
- `concert`: data i lloc (18 juny 2027, Estadi Olímpic). L'hora no hi surt fins que sigui oficial.
- `ticketLabel`: «Val per 1 entrada». Quan tinguis les entrades, canvia-ho.

## 2b. Els vals que exploten
A `GIFT.vouchers` (bloc de configuració) hi ha les dades de cada un dels sis regals, en l'ordre de les targetes: `rows:[['Lloc','...'],['Data','...'],['Inclou','...'],['Condicions','...']]`. Pots canviar-ne el text o afegir-hi files. La durada (10 s) són la `animation` de `.v-bar` (CSS, `10s`) i el comptador del JS (`let n=10`).

## 3. Recorregut
Cartró de rasca i guanya (ella rasca; el botó «Ensenya-m’ho» l’obre directament) → sis regals: ella en descarta tres → n'escull un de tres → **apareix el val del regal amb lloc, data, què inclou i condicions, i durant 10 segons sembla de veritat; quan arriba a zero explota** i surt «Que no! Ai, pobreta. T’ho has cregut?» → compte enrere → revelació amb la música → targeta-promesa, vídeo, carta, dies que falten i botons.
Botons: **Afegeix-ho al calendari** (.ics amb avís 30 min abans de la venda i el dia del concert), **Desa-la** (imatge de la targeta), **Comparteix** (enllaç, un cop publicada) i **Torna a començar**.

## 4. Disseny
Tipografia basada en estopa.com: Allerta Stencil, Oswald, Anton (equivalent a Impact) i Open Sans. Fonts incloses a `fonts/` (llicències a `fonts/LICENSES.txt`). No s'utilitza cap logotip ni imatge d'Estopa.
