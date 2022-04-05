---
layout: base
title:  'Pomak-Philotis UD'
udver: '2'
---

# Universal Dependencies for Pomak
<!--<span class="flagspan"><img class="flag" src="pm.png"/></span>-->

## Tokenization and Word Segmentation


* In general, words are delimited by whitespace characters and every single token is segmented separately. For example: _za da_ "in order to", _ní kutrí_ "no one", _zablǽvom so_ "slow myself".
* The numbers are analyzed as one token when used as expression without spaces (20000) or with an internal comma as indicator (10,434).


## Morphology

### Tags

This is an overview only. For a more detailed discussion and examples, see the list of [Pomak POS tags](pos/index.html) and [Pomak features](feat/index.html).

* Pomak treebank uses 16 universal POS categories. Currently it does not make use of [SYM](../../u/pos/SYM.html).
* Affirmative, negative, interrogative, modal particles are analyzed as [PART](pos/PART.html).
* [PRON](pos/PRON.html) are distinguished from [DET](pos/DET.html) as follows:
	* Both the strong and the weak types of personal pronouns (_ja/mí/mó, ty/tí/tó, toj/mú/go, tja/jí/jé, to/mú/go, nýje/nú/nú, výje/vú/vú, tíje/mí/gi, to/mí/gi_) are assigned the PoS tag [PRON](pos/PRON.html).
	* The weak types of possessive pronouns (_mi, ti, mu, ji, nu, vu, mi_) are assigned the PoS tag [PRON](pos/PRON.html).
	* The reflexive pronouns  `sá/sé/só` και `sí` are assigned the PoS tag [PRON](pos/PRON.html).
	* Then pronoun types _kaná_ "what", _kanása / kanáta / kanána_ "whatever here - proximal / whatever there -medial / whatever over there - distal", _ní kaná_ "nothing" and _síčko / síčkoso / síčkoto / síčkono_ "all / everything" are assigned the PoS tag [PRON](pos/PRON.html).
	* The strong types of possessive pronouns (_moj, tvoj, tógav, tójin, naš, vaš, tǽhan_) and all other pronouns are assigned the PoS tag [DET] (pos/DET.html).
	* The adjective _adín/edín/idín_ is assigned the PoS tag [DET](pos/DET.html) when it is used as an indefinite article.

* Pomak has only one auxiliary verb ([AUX](pos/AUX_.html)), _som_ (“to be”), but lemmas such as _býdom_ are also possible.
* Τhe auxiliary verb šom / štom (δυνητικό θα) is assigned the PoS tag [AUX](pos/AUX_.html).
* Auxiliary particles _še / ša_ ("will, shall") and _da_ ("to") are assigned the PoS tag [AUX](pos/AUX_.html).
* Modal verbs are assigned the PoS tag [VERB](pos/VERB.html).
* The  PoS tag [ADJ](pos/ADJ.html) is assigned to adjectives, ordinal numerals, adjectives derived from family names and ethnonyms.
* The  PoS tag  [VERB](pos/VERB.html) is assigned to personal and impersonal verbs, participles, infinitives and converbs.
* <b><u>Note</u></b>: Pomak has a triple post-positioned definite article which is part of the word that receives no distinct PoS tag.


### Features

* Features currently NOT used: [Typo](), [NounClass](), [Evident](), [Polite](), [Clusivity]().

#### Nominal Features

* Common nouns ([NOUN](pos/NOUN.html)) and proper nouns ([PROPN](pos/PROPN.html)) have inherent gender ([Gender](feat/Gender.html)) that receives one of the following values: `Masc`, `Fem` ή `Neut`.
* [Animacy](feat/Animacy.html) is a grammatical feature of pronouns, adjectives, participles and some of the numerals. The opposition  `Human vs. Non-human` is overt with  masculine plural and rarely  with masculine singular.
*  [ADJ](pos/ADJ.html), [DET](pos/DET.html), [NUM](pos/NUM.html), the participles that are assigned the PoS tag [VERB](pos/VERB.html) και [PRON](pos/PRON.html) inflect for [Case](feat/Case.html), gender [Gender](feat/Gender.html) and number [Number](feat/Number.html) and agree with the nouns that they modify.
	* <b><u>Note</u></b>: Certain adjectives (of turkish origins mainly) do not inflect.
* Pomak has four cases: Nominative, Genitive, Accusative and Vocative.
* Pomak nouns, adjectives, certain numerals, passive participles and the strong types of pronouns may be marked for the feature [Definite](feat/Definite.html).  When an article is attached to them they are assigned the value `Def` else the value `Ind`.
* Pomak has a triple enclitic definite artile (-s, -t, -n) that occurs with nouns, adjectives, pronouns and passive participles.  Για τη σήμανση του χρησιμοποιούνται τα features [Deixis](feat/Deixis.html) και [DeixisRef](feat/DeixisRef.html) ως εξής:
	* Proximity to the speaker is denoted with the values  `Prox` and `1` respectively (e.g., _čulǽk<u>os</u>, žaná<u>sa</u>, déte<u>so</u>_).
	* Proximity to the listener is denoted with the values  `Prox` and `2` respectively (e.g., _čulǽk<u>ot</u>, žaná<u>ta</u>, déte<u>to</u>_).
	* Distance from both the speaker and the listener is denoted with the value `Remt` (e.g., _čulǽk<u>on</u>, žaná<u>na</u>, déte<u>no</u>_).


#### Degree and Polarity

* The comparative and superlative degree of adjectives and adverbs is formed with the adverbs  _po_ and _naj_ respectively: they both are distinct words.   Τhe feature [Degree](feat/Degree.html) is used to denote the positive, comparative and superlative degre of adjectives and adverbs and is assigned one of the values  `Pos`, `Cmp` και `Sup` respectively. Only the comparative and the superlative degree have been declared so far while the positive degree is treated as the default. 
* [Polarity](feat/Polarity.html) has two values, `Pos` and `Neg`, and applies primarily to negative and affirmative particles [PART](pos/PART.html).  So far, only the value  `Neg` has been used.

#### Verbal Features

* Similarly to other Slavic languages, Pomak verbs are marked for  [Aspect](feat/Aspect.html) as a lexically classifying feature, that takes one of the following four values: `Imp`, `Perf`, `Iter`, `Prog`.
* Finite verbs always are marked for one of two values of [Mood](feat/Mood.html): `Ind` or `Imp`, one of four values of [Number](feat/Number.html): `Sing`, `Plur`, `Count` or `Coll` and one of three values of [Person](feat/Person.html): `1`, `2` or `3`.
* Verbs in the `Ind` mood are always  marked forone of two values of [Tense](feat/Tense.html): `Past` or `Pres`. `Fut` is not used because this tense is always formed with a special particle.
* Finite verbs of the `Imp` mood have only 2nd [Person](feat/Person.html).
* There are two values of the [Voice](feat/Voice.html) feature: `Act` and `Pass`. Only the passive participle has `Voice=Pass`. All other verb forms have `Voice=Act`.
* There are three types of nonfinite verb forms ([VerbForm](feat/VerbForm.html)): `Conv`, `Inf` and `Part`.

#### Pronouns, Determiners, Quantifiers

* [PronType](feat/PronType.html) is used with pronouns ([PRON](pos/PRON.html)), determiners ([DET](pos/DET.html)) and adverbs ([ADV](pos/ADV.html)).
* [NumType](feat/NumType.html) is used with numerals ([NUM](pos/NUM.html)), adjectives ([ADJ](pos/ADJ.html)).
* The [Poss](feat/Poss.html) feature marks possessive personal determiners (e.g. _moj_ “my”), possessive interrogative (indefinite or negative) determiners (e.g., _číjje_ “whose”), possessive relative determiners (e.g., _číjjeso, číjjeto, číjjeno_ “whose”) and possessive adjectives (e.g., _májčin_ “mother's”).
	* <b><u>Note</u></b>: Indefinite, negative and universal pronouns  (e.g., _ní kutrí_ "no one") and indefinite, negative and universal adjectives (e.g., _ní kadé_ "no where") are formed with the particles `nǽ / nó, ní, sǽ` and the corresponding interogative pronoun. The particles precede the pronouns and retain both their word status and the feature `PronType=Int`.
* The [Reflex](feat/Reflex.html) feature is assigned to reflexive pronouns _`sá, sé, só`_ and possesive clitic pronoun _`sí`_.
* [Person](feat/Person.html) is a lexical feature of personal pronouns ([PRON](pos/PRON.html)) and personal determiners ([DET](pos/DET.html)) and has three values: `1`, `2` and `3`.
* There is one [layered feature](../../u/overview/feat-layers.html), namely [Number[psor]](feat/Number-psor.html).
  It appears with the possesive determiners and encodes the lexical number of the possessor.
  The extra layer is needed to distinguish this lexical feature from the inflectional number that marks agreement with the modified (possessed) noun.

### Other Features

* Language-specific features of Pomak:

  * Diminutive and augmentative forms of nouns, adjectives, adverbs and certain passive participles are assigned the feature [qpm-DegreeMod](feat/qpm-DegreeMod.html) and onee of the values `Dim` ή `Mag` respectively.

  * Τhe feature [Variant](feat/Variant.html) with the value `Short` is assigned to the weak types of personal and possessive pronouns to set them apart from their corresponding strong types.  

  * Τhe particles `nǽ` / `nó`, `ní`, `sǽ`, which are used to form the indefinite, negative and universal pronouns and adverbs, are assigned the PoS tag  [PART](pos/PART.html) and the feature [qpm-PartType](feat/qpm-PartType.html) with one of the following values `Ind`, `Neg` ή `Tot` respectively.

## Syntax

Only the morphological annotation of the treebank has been studied in detail so far. 
The syntactic annotation was obtained with the Udify tools. An updated version of the treebank with a fully studied syntactic annotation 
is estimated to be uploaded at the end of 2022.

<!--- This is an overview only. For more detailed discussion and examples, see the list of [Pomak relations](dep/index.html).-->

### Core Arguments, Oblique Arguments and Adjuncts


### Other relations:


### No used relations:--->


## Treebanks

There is 1 Pomak UD treebank:

  * [Pomak-Philotis](index.html)
