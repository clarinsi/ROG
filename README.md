# ROG - Ročno označeni govor (Manually annotated speech)

## Structure:

ROG consists of 57 manually annotated recordings from the Artur corpus (`ROG-Art`) and CONLLU files of the same 57 recordings plus additional 287 CONLLU files from the GOS corpus.


```
ROG
├── DOCS
│   ├── ROG-speakers.tsv
│   └── ROG-speeches.tsv
├── PREBERIME.md
├── README.md
├── ROG-TrainDevTest-split.tsv
├── ROG-Art
│   ├── ROG-Art-TrainDevTest-split.tsv
│   ├── EXB  [57 entries]
│   ├── EXS  [58 entries]
│   ├── TRS  [114 entries]
│   ├── TXT  [114 entries]
│   └── WAV  [57 entries]
└── ROG-UD  [344 entries]
```
ROG consists of two directories: `CONLLU` and `ROG-Art`. `CONLLU` directory contains 344 conllu files, while `ROG-Art` is split in subdirectories based on the file types (AVD for audio, TXT for text, ...)

## Metadata

Metadata is available for 344 CONLLU files, and separately for the 57 files in the ROG-Art directory. The structure of both variants is the same:

### `ROG-speakers.tsv`

Describes speakers appearing in recordings, and contains columns:

* TEXT-ID: Recording identifier, as used in this corpus
* SOURCE-ID: Recording identifier, as used in their original corpora
* RECORDING-ID: Original recording name
* SUBCORPUS: Subcorpus in GOS2.1 from where the instance was sampled (Gos/Artur-J/Artur-N/Artur-P)
* PRS-ID: Speaker ID
* SEX: Speaker sex
* AGE: Speaker age
* 1LANG: First language of the speaker
* DIALECT: Additional details on the language the speaker is using (described with labels like standardni, pogovorni, narečje, tujejezični vplivi...)
* EDUCATION: Speaker education
* PERM-RESD: Region where the speaker resides
* CHILD-RESD: Region where the speaker lived as a child
* SENTENCES: Number of sentences said by the speaker in the recording
* WORDS: Number of words said by the speaker in the recording.

Minus (`-`) was used to indicate missing values.

### `ROG-speeches.tsv`

Describes recordings and contains columns:

* TEXT-ID: Recording identifier, as used in this corpus
* SOURCE-ID: Recording identifier, as used in their original corpora
* RECORDING-ID: Original recording name
* SUBCORPUS: Subcorpus in GOS2.1 from where the instance was sampled (Gos/Artur-J/Artur-N/Artur-P)
* TITLE: Description of the recording topic
* DATE: Year and month of the recording
* SOURCE: Recording source, e.g. title of the TV programme from which the speech was sampled
* URL: Recording URL
* TEXT-REGION: Location of the recording
* DOMAIN
* TYPE:
* CHANNEL: Communication channel (e.g. TV / radio / personal contact)
* SENTENCES: Number of sentences
* WORDS: Number of words
* SPK-IDsUTTS: Identifiers of all speakers that appear in the recording

Minus (`-`) was used to indicate missing values.


### `ROG-TrainDevTest-split.tsv`

Describes composition of train, dev, and test subsets. Contains columns:
* TEXT-ID: Recording identifier
* Split: Subset (Train, Dev, Test)


# Dublin core

| parameter      | suggestion                                                                                                  | definition                                                                                                                                                                                                                                                  |
| -------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DC:title       | ROG                                                                                                         | The name of your website                                                                                                                                                                                                                                    |
| DC:source      | https://www.clarin.si/repository/xmlui/handle/11356/1863                                                    | Where the content originally delivered from or a resource that is related intelectually to the described content.                                                                                                                                           |
| DC:coverage    | ?Slovenia?                                                                                                  | Where the content is physically located. Coverage will typically include spatial location (place name or geographic co-ordinates), temporal period (date, date range) or jurisdiction (named administrative entity).                                        |
| DC:description | Manually annotated corpus of spoken Slovene...                                                              | Textual outline of the content. Can be the same as the content of <meta name="descripion"> tag.                                                                                                                                                             |
| DC:subject     | ?Linguistics, Spoken Slovenian, Corpus Linguistics, Disfluency Analysis, Prosody, Dialog Act, Morphosyntax? | The topic covered by the content.                                                                                                                                                                                                                           |
| DC:creator     | Darinka Verdonik                                                                                            | The person or organization responsible for the content.                                                                                                                                                                                                     |
| DC:type        | corpus                                                                                                      | A category for the content. A full list of Types can be found [here](http://dublincore.org/documents/dcmi-type-vocabulary/#dcmitype-Collection)                                                                                                             |
| DC:publisher   | CLARIN.si, UM, IJS, UL...                                                                                   | An entity (person, organization or service) responsible for making the content available.                                                                                                                                                                   |
| DC:rights      | Creative Commons - Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)                                  | Typically a Rights element will contain a rights management statement for the resource, or reference a service providing such information. Rights information often encompasses Intellectual Property Rights (IPR), Copyright, and various Property Rights. |
| DC:relation    | ?                                                                                                           | How the content relates to other resources for instance. Think in a chapter of a book, for example: the chapter isPartOf book. A full list of possible relations can be found [here](https://paladini.github.io/dublin-core-basics/)                        |
| DC:date        | (trivial)                                                                                                   | A point or period of time associated with the lifecycle of content. Typically the date of when content become available.                                                                                                                                    |
| DC:format      | Text/Plain, Text/XML, Audio/WAV                                                                             | Types are available [here](http://dublincore.org/documents/dcmi-type-vocabulary/#dcmitype-Collection)                                                                                                                                                       |
| DC:language    | slv                                                                                                         | In what language the content is written. You must the correct language code. You can find all language codes [here](https://paladini.github.io/dublin-core-basics/).                                                                                        |
| DC:contributor | vsi deležniki                                                                                               | Person, organization or service that contribute to the content.                                                                                                                                                                                             |
| DC:indentifier | hdl.handle.net...                                                                                           | An unique identifier to your content. Can be a string or number generate by a formal identification system - or just a URL.                                                                                                                                 |