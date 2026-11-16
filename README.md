# Mat.Tone

**Una groovebox per fare rap e hip hop dall'idea al pezzo finito: pad, sequencer, canzone, testi, voce e mix in un'unica app.**

Mat.Tone ha l'aspetto di un campionatore vintage da cantina, con lo schermino, le lancette e i pad di gomma. Dentro però c'è tutto quello che serve per chiudere un brano: dai la batteria con le dita, scrivi le rime, registri la voce sul beat e lo esporti al volume giusto per Spotify. Funziona come app per PC (Windows, Mac, Linux) e anche dal browser, sul computer e sul telefono.

## Scaricare

Dalla pagina [Releases](https://github.com/Akaoni97/Mat.Tone/releases) prendi l'ultima versione `mattone-v…`:

| Sistema | File |
|---|---|
| Windows | `Mat.Tone-Setup-<versione>.exe` (si installa e si aggiorna da solo) oppure `Mat.Tone-Portatile-<versione>.exe` (senza installazione) |
| Mac | `Mat.Tone-<versione>-arm64.dmg` (al primo avvio: clic destro sull'app → Apri) |
| Linux | `Mat.Tone-<versione>.AppImage` (si aggiorna da solo) |

L'app per PC funziona offline: suoni, font e codificatore MP3 sono inclusi. All'avvio controlla se c'è una versione nuova.

## Cosa fa

**Suona**
- 4 gruppi da 12 pad (batteria, percussioni, strumenti, synth), suonabili col mouse, col dito, con la tastiera del computer o con un controller MIDI.
- Oltre 600 suoni e 26 kit pronti: boom bap, lo-fi, trap, West Coast, old school, tekno, free party, jazz, soul. Ci sono batterie acustiche con dinamiche vere e round robin, e 66 strumenti campionati su tre ottave.
- Modalità Note e Tastiera per suonare melodie sulla scala scelta; synth polifonico con 14 suoni; accordi e arpeggi.
- Campiona dal microfono, carica i tuoi file, taglia i loop in pezzi sui pad. Le cartelle dei tuoi campioni si sfogliano dall'app per PC.
- Effetti al volo da tenere premuti, note repeat, colpi «mai uguali» come un batterista vero.

**Sequencer e canzone**
- Pattern da 1, 2 o 4 battute, a sedicesimi o a terzine. Si scrive trascinando sulla riga, con copia e incolla di battute e righe e «Raddoppia».
- Tocco lungo su un passo per accento, nota fantasma, rullata, probabilità e impostazioni del singolo passo; groove alla MPC, swing per gruppo, mano umana.
- Assistente melodia (accordi, melodie, basso 808), «Canticchia» dal microfono, e **Beatbox → batteria**: fai il ritmo con la bocca e diventa cassa, rullante e charleston.
- Canzone a sezioni (Intro, Strofa, Ritornello…), con i colori e il trascinamento di parti e sezioni intere. «Fammi la canzone» la costruisce da un pattern.
- Passaggi automatici e registrazione della performance dal vivo.

**Testi**
- Il quaderno del rap: una riga per battuta, con accanto la sezione e le sillabe di ogni riga.
- Rime in italiano (perfette e assonanze) da circa 40.000 parole, che si scrivono con un clic.
- Il testo segue il beat mentre suona, e nella pagina Voce scorre come un gobbo.

**Voce**
- Registra il rap sul beat con click d'attacco e preroll; rifai solo le battute sbagliate.
- **Voce migliore:** scegli battuta per battuta la presa migliore tra più prese. **Doppie** e **ad-lib** suonano ai lati della voce principale.
- Catena voce con de-esser, compressore, calore, filtri (telefono, radio, cassetta), eco e riverbero; autotune dal vivo e sulle prese.

**Mix ed esportazione**
- Banco a 4 gruppi e master con saturazione, nastro, colla, pompa sulla cassa e limiter (picchi mai sopra −1 dB), con misura del volume in LUFS.
- **Pronto per Spotify:** ascolta il pezzo e lo porta da solo a −14 LUFS.
- Esporta in MP3 e WAV, video per i social (verticale, quadrato, orizzontale), tracce separate per il DAW, file MIDI e progetto completo.

**I miei beat**
- Tutti i beat salvati da soli mentre lavori, con anteprima; si aprono, rinominano e duplicano.
- «Nuovo beat» da uno stile in un clic.
- Esporta e importa tutti i beat in un file, per passare dal telefono al PC.

**E poi**
- Lato B: un giradischi da battaglia con crossfader per lo scratch.
- Modalità **Semplice** (solo l'essenziale) e **Completa** (tutti i comandi).
- Scocche e aspetto personalizzabili, vista 3D.
- Modalità leggera sul telefono, anche in orizzontale.

## Com'è fatto

```
mattone.html      tutta l'app in un solo file (HTML, CSS, JavaScript, Web Audio)
suoni/            i suoni: pacchetti e campioni grandi
desktop/          l'app per PC (Electron): vedi desktop/README.md
```

Non ci sono framework né passaggi di compilazione per la parte web: `mattone.html` si apre direttamente nel browser. Il motore audio usa Web Audio e AudioWorklet (limiter con look-ahead, autotune, piatto). Le versioni per PC vengono compilate e pubblicate dal workflow `.github/workflows/mattone-desktop.yml` quando cambia la versione in `desktop/package.json`.

Fino alla versione 1.0.59 Mat.Tone viveva nel repository [RandomEgg-s](https://github.com/Akaoni97/RandomEgg-s), da cui è stato spostato con tutta la sua cronologia.

## Crediti

I suoni vengono da librerie libere, ognuna con la sua licenza (CC0, CC BY, CC BY-SA): l'elenco completo è nella pagina **Guida** dell'app. Il codificatore MP3 è [lamejs](https://github.com/zhuker/lamejs) (LGPL-3.0). Le rime vengono dall'elenco di parole [FrequencyWords](https://github.com/hermitdave/FrequencyWords) di Hermit Dave (OpenSubtitles, CC BY-SA 4.0).
