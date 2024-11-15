# ROG - Ročno označeni govor (Manually annotated speech)

## Structure:

ROG je sestavljen iz 57 ročno označenih posnetkov iz korpusa Artur (v direktoriju `ROG-Art`) in CONLLU datotek istih 57 posnetkov in dodatnih 287 primerov iz korpusa Gos.


```
ROG
ROG
├── DOCS
│   ├── ROG-speakers.tsv
│   └── ROG-speeches.tsv
├── PREBERIME.md
├── README.md
├── ROG-TrainDevTest-split.tsv
├── ROG-Art
│   ├── ROG-Art-TrainDevTest-split.tsv
│   ├── EXB  [57 datotek]
│   ├── EXS  [58 datotek]
│   ├── TRS  [114 datotek]
│   ├── TXT  [114 datotek]
│   └── WAV  [57 datotek]
└── ROG-SST  [344 datotek]
```

Korpus ROG sestavljata direktorija `CONLLU` in `ROG-Art`. `CONLLU` vsebuje 344 datotek v formatu `conllu`, `ROG-Art` pa je razdeljen na direktorije po tipu datotek.

## Metapodatki

Metapodatki so na voljo za 344 primerov CONLLU datotek, vrstice, ki opisujejo 57 ročno označenih datotek, pa so na voljo tudi ločeno v direktoriju ROG-Art. V obeh primerih je struktura enaka:

### `ROG-speakers.tsv`

Popisuje govorce, ki nastopajo v posameznem posnetku. Vsebuje stolpce:

* TEXT-ID: Identifikator posnetka, kot se uporablja v trenutnem korpusu
* SOURCE-ID: Identifikator posnetka v izvornem korpusu
* RECORDING-ID: Izvorno ime posnetka
* SUBCORPUS: Podkorpus v korpusu Gos2.1, v katerem se nahaja izvorni posnetek (Gos/Artur-J/Artur-N/Artur-P)
* PRS-ID: Identifikator govorca
* SEX: Spol govorca
* AGE: Starost govorca
* 1LANG: Materni jezik govorca
* DIALECT: Dodatni opis jezika govorca (standardni, pogovorni, narečje, tujejezični vplivi...)
* EDUCATION: Izobrazba govorca
* PERM-RESD: Regija prebivališča govorca
* CHILD-RESD: Rojstna regija govorca
* SENTENCES: Število stavkov, ki jih govorec izreče v posnetku
* WORDS: Število besed, ki jih govorec izreče v posnetku.

Za manjkajoče podatke je uporabljen minus: `-`

### `ROG-speeches.tsv`

Popisuje posnetke. Vsebuje stolpce:

* TEXT-ID: Identifikator posnetka, kot se uporablja v trenutnem korpusu
* SOURCE-ID: Identifikator posnetka v izvornem korpusu
* RECORDING-ID: Izvorno ime posnetka
* SUBCORPUS: Podkorpus v korpusu Gos2.1, v katerem se nahaja izvorni posnetek (Gos/Artur-J/Artur-N/Artur-P)
* TITLE: Opis govora
* DATE: Leto in mesec snemanja
* SOURCE: Vir, na primer naziv oddaje, iz katere posnetek prihaja
* URL: Url posnetka
* TEXT-REGION: Mesto, kjer je posnetek nastal
* DOMAIN: Dodatni opis
* TYPE: Dodatni opis
* CHANNEL: Način prenosa govora (radio, TV, osebni stik...)
* SENTENCES: Število stavkov v posnetku
* WORDS: Število besed v posnetku
* SPK-IDsUTTS: Identifikatorji govorcev, ki nastopajo v posnetku

Za manjkajoče podatke je uporabljen minus: `-`

### `ROG-TrainDevTest-split.tsv`

Opisuje, v kateri podmnožici (učna, testna, razvijalna) se nahajajo posnetki. Vsebuje stolpce:
* TEXT-ID: Identifikator posnetka
* Split: Podmnožica (Train, Dev, Test)