<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

En Deel vum Websäit Code ass Open Source, wëllkomm fir ze hëllefen d'Iwwersetzung ze optimiséieren.

## Front-Enn Code

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
