<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.adwinni

Wɛbsaet koodu no fã bi yɛ open source, yɛma wo akwaaba sɛ ɛbɛboa ma nkyerɛase no ayɛ papa.

## anim-awieɛ koodu

* [anim-awieɛ koodu](https://github.com/xxai-art/web)
* [Kasa packs ma site no nyinaa](https://github.com/xxai-art/web/tree/main/i18n)
* [Kasa packs a wɔde yɛ login modules](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Wɛbsaet Kasa Ahorow Nkyerɛwee](https://github.com/xxai-doc)

Anim-awieɛ dwumadie kasa ne [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , a ɛde nneɛma bi a egyina coffeescript syntax so ka ho, hwɛ [./coffee_plus.md](./coffee_plus.md) .

## Amanaman ntam nkitahodi a wɔde bɛyɛ wɛbsaet ne nkrataa

Fa nnwuma 3 a edidi so yi si hɔ

* [@w5/mdt na ɛwɔ hɔ](https://www.npmjs.com/package/@w5/mdt)

  Suffix no yɛ `.mdt` , wobɛtumi de syntax a ɛte sɛ `<+ ./coffee_plus/import.js>` adi dwuma de akyerɛ abɔnten fael, na wode subffix `.md` ayɛ markdown.

* [@w5/trmd na ɛwɔ hɔ](https://www.npmjs.com/package/@w5/trmd)

  Markdown nkyerɛaseɛ renkyerɛ koodu ne link ase, na ɛbɛkora kasamu a wɔakyerɛ aseɛ no so. Sɛ wɔayɛ nsakrae wɔ nkyerɛase no mu nanso wɔansakra mfitiase nkyerɛwee no a, sɛ wosan yɛ no bio a, ɛrenkyerɛw nkyerɛase no mu nsakrae no so.

* [@w5/i18n na ɛwɔ hɔ](https://www.npmjs.com/package/@w5/i18n)

  Kasa fael a wɔde kyerɛ wɛbsaet ahorow `yaml` ayɛ ase.

### Nwoma Nkyerɛaseɛ Automation Akwankyerɛ

Hwɛ adekorabea [xxai-art/doc](https://github.com/xxai-art/doc)

Wɔhyɛ nyansa sɛ wobɛdi kan ahyɛ nodejs, [direnv](https://direnv.net) ne [bun](https://github.com/oven-sh/bun) , na afei woayɛ `direnv allow` bere a woahyɛn directory no mu awie no.

Sɛnea ɛbɛyɛ a mɛkwati adekoradan akɛse dodo a wɔakyerɛ ase akɔ kasa ɔhaha pii mu no, meyɛɛ mmara adekoradan a ɛyɛ soronko maa kasa biara na meyɛɛ ahyehyɛde bi a wɔde besie adekoradan yi

Sɛ wo hyehyɛ atwa yɛn ho ahyia nsakraeɛ `GITHUB_ACCESS_TOKEN` na afei wotu [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) a, ɛbɛbɔ adekoradan no ara.

Nokwarem no, wubetumi de ahyɛ adekoradan mu nso.

Nkyerɛase script nkyerɛkyerɛmu [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Wɔkyerɛ script code no ase sɛnea edidi so yi:

[bunx](https://bun.sh/docs/cli/bunx) yɛ npx ananmu, a ɛyɛ ntɛmntɛm. Nokwarem no, sɛ wo nni bun a wɔde ahyɛ mu a, wubetumi de `npx` adi dwuma mmom.

`bunx mdt zh` kyerɛ `.mdt` wɔ zh directory no mu sɛ `.md` , hwɛ fael 2 a ɛka bom wɔ aseɛ ha

* [kɔfe_a wɔde ka ho.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [kɔfe_a wɔde ka ho.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` yɛ core code ma nkyerɛaseɛ (sɛ wowɔ `nodejs` nko ara a wɔde ahyɛ mu, nanso `bun` ne `direnv` nhyɛ mu a, wobɛtumi nso ayɛ `npx i18n` de akyerɛ aseɛ).

Ɛbɛpaapae [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , nhyehyɛe a ɛwɔ `i18n.yml` mu wɔ krataa yi mu no te sɛ nea edidi so yi:

```
en:
zh: ja ko en
```

Nea ɛkyerɛ ne sɛ: China kasa mu nkyerɛase kɔ Japan, Korea, Borɔfo, Borɔfo nkyerɛase mu kɔ kasa afoforo nyinaa mu. Sɛ wopɛ sɛ woboa China ne Borɔfo kasa nkutoo a, wubetumi akyerɛw `zh: en` kɛkɛ.

Nea etwa to ne [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , a ɛyi nsɛm a ɛwɔ asɛmti titiriw ne kasa biara `README.md` asɛmti ketewa a edi kan no ntam de yɛ nsɛm a wɔakyerɛw `README.md` . Code no yɛ mmerɛw yiye, w’ankasa wubetumi ahwɛ.

Wɔde Google API di dwuma ma nkyerɛase a wontua hwee. Sɛ wo ntumi nkɔ Google a, yɛsrɛ wo hyehyɛ na hyehyɛ proxy, te sɛ:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Nkyerɛaseɛ script no bɛma nkyerɛaseɛ cache wɔ `.i18n` directory mu, yɛsrɛ wo hwɛ no ne `git status` na fa ka code repository no ho na woakwati nkyerɛaseɛ mpɛn pii.
