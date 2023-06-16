<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Et ass recommandéiert nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) zuerst z'installéieren, an dann `direnv allow` nodeems Dir an de Verzeichnis eragitt ( [den .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) gëtt automatesch ausgefouert nodeems Dir de Verzeechnes eragitt).

D'Bedeitung ass: Chinesesch Iwwersetzung op Japanesch, Koreanesch, Englesch, Englesch Iwwersetzung an all aner Sproochen. Wann Dir nëmmen Chinesesch an Englesch wëllt ënnerstëtzen, kënnt Dir einfach `zh: en` .

D'Bedeitung ass: Chinesesch Iwwersetzung op Japanesch, Koreanesch, Englesch, Englesch Iwwersetzung an all aner Sproochen. Wann Dir nëmmen Chinesesch an Englesch wëllt ënnerstëtzen, kënnt Dir einfach `zh: en` .

* [Front-Enn Code](https://github.com/xxai-art/web)
* [Sproochepäck fir de Site als Ganzt](https://github.com/xxai-art/web/tree/main/i18n)
* [Sproochepak fir Login Moduler](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Websäit Multilingual Dokumentatioun](https://github.com/xxai-doc)

D'Front-End Programméierungssprooch ass [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , déi e puer Features bäidréit baséiert op der Coffeescript Syntax, kuckt [./coffee_plus.md](./coffee_plus.md) .

## Internationaliséierung vun Websäiten an Dokumenter

Baut op déi folgend 3 Projeten

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  De Suffix ass `.mdt` , Dir kënnt d'Syntax ähnlech wéi `<+ ./coffee_plus/import.js>` benotze fir op extern Dateien ze referenzéieren, a Markdown mat dem Suffix `.md` .

* [@w5/eng](https://www.npmjs.com/package/@w5/trmd)

  Markdown Iwwersetzung wäert keng Coden a Linken iwwersetzen, a wäert iwwersat Sätz cache. Wann d'Iwwersetzung geännert gëtt, awer den ursprénglechen Text net geännert gëtt, wäert d'Ännerung vun der Iwwersetzung net iwwerschreiwe wann Dir se nach eng Kéier ausféiert.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Sproochdateien fir iwwersetze `yaml` generéiert Websäiten.

### Dokument Iwwersetzung Automatioun Instruktioune

Kuckt Code Repository [xxai-art/doc](https://github.com/xxai-art/doc)

Et ass recommandéiert nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) zuerst z'installéieren, an dann `direnv allow` nodeems Dir an de Verzeichnis eragitt ( [den .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) gëtt automatesch ausgefouert nodeems Dir de Verzeechnes eragitt).

Fir déi grouss Codebasis ze vermeiden, déi an Honnerte vu Sproochen iwwersat gëtt, hunn ech eng separat Codebasis fir all Sprooch erstallt an eng Organisatioun erstallt fir de Codebasis ze späicheren

D'Ëmfeldsvariabel `GITHUB_ACCESS_TOKEN` setzen an dann [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) lafen erstellt automatesch de Code Repository.

Natierlech kënnt Dir et och an enger Codebasis setzen.

Iwwersetzung Schrëft Referenz [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

De Skriptcode gëtt wéi follegt interpretéiert:

[bunx](https://bun.sh/docs/cli/bunx) ass en Ersatz fir npx, wat méi séier ass. Natierlech, wann Dir kee Bun installéiert hutt, kënnt Dir `npx` amplaz benotzen.

`bunx mdt zh` rendert `.mdt` am zh Verzeichnis als `.md` , kuckt déi 2 verlinkte Dateien hei drënner

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ass de Kärcode fir Iwwersetzung (wann Dir nëmmen `nodejs` installéiert hutt, awer `bun` an `direnv` sinn net installéiert, Dir kënnt och `npx i18n` lafen fir ze iwwersetzen).

Et wäert [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) parséieren, d'Konfiguratioun vun `i18n.yml` an dësem Dokument ass wéi follegt:

```
en:
zh: ja ko en
```

D'Bedeitung ass: Chinesesch Iwwersetzung op Japanesch, Koreanesch, Englesch, Englesch Iwwersetzung an all aner Sproochen. Wann Dir nëmmen Chinesesch an Englesch wëllt ënnerstëtzen, kënnt Dir einfach `zh: en` .

Déi lescht ass [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , déi den Inhalt tëscht dem Haapttitel an dem éischten Ënnertitel vun `README.md` vun all Sprooch extrahéiert fir en Entrée `README.md` ze generéieren. De Code ass ganz einfach, Dir kënnt et selwer kucken.

Google API gëtt fir gratis Iwwersetzung benotzt. Wann Dir keng Zougang zu Google hutt, da konfiguréiert a setze w.e.g. e Proxy, wéi:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

D'Iwwersetzungsskript generéiert en iwwersat Cache am `.i18n` Verzeichnis, kontrolléiert et w.e.g. mam `git status` a füügt et an de Code Repository fir widderholl Iwwersetzungen ze vermeiden.

Fuert w.e.g. `bunx i18n` all Kéier wann Dir d'Iwwersetzung ännert fir de Cache ze aktualiséieren.

Wann den ursprénglechen Text an d'Iwwersetzung gläichzäiteg geännert ginn, gëtt de Cache duercherneen, also wann Dir wëllt änneren, kënnt Dir nëmmen een änneren, an dann `bunx i18n` lafen fir de Cache ze aktualiséieren.
