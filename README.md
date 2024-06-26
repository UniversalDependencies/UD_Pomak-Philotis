# Summary

The Pomak UD treebank  is derived from the Pomak Dependency Treebank,
a resource developed and maintained by researchers at the Institute for Language and Speech Processing/Athena
R.C. (http://www.ilsp.gr).

# Introduction

The Pomak UD treebank consists of 6351 sentences (86782 tokens). The
data in the current release derive from primary texts that will be made available soon on the repositories of the Philotis project (https://www.ilsp.gr/en/projects/filotis-en/). The treebank is licensed under the terms of [Creative
Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)
](https://creativecommons.org/licenses/by-nc-sa/4.0/).


The morphological annotation of the Pomak UD treebank
was originally created by applying the morphological database Rodopsky to the texts and then by extensive manual correction by two annotators.
The syntactic annotation of the 1.1
release was generated automatically using a Bulgarian model. A detailed revision of the automatic syntactic annotation is due at the end of 2022.

# Acknowledgments

We wish to thank all contributors to the original annotation
efforts. Morphological annotation was carried out by Ritvan Karahoǧa and Nicolaos Constantinides. Panagiotis Krimpas supported the annotation with expertise in Slavic languages and Stella Markantonatou with expertise in formal grammatical frameworks. Nicolaos Kokkas contributed to the collection of Pomak texts.

## References

* Karahóǧa, R. Krimpas, P., Stamou, V., Arampatzakis, V., Karamatskos, D., Sevetlidis, V.,  Constantinides, N., Kokkas, N., Pavlidis, G., Markantonatou,S. (2022). Morphologically annotated corpora of Pomak. In Proceedings of the 5th Workshop on the Use of Computational Methods in the Study of Endangered Languages: The Use of Computational Methods in the Study of Endangered Languages. Association for Computational Linguistics. Dublin, May 26-27, 2022.

# Data splits

- Train/dev/test sets: 5080/635/635 sentences, 69287/9085/8410 tokens


# Changelog

* 2023-05-15 v2.12
  * Feature DegreeModQpm replaced with universal Degree (diminutives, augmentatives).
* 2022-04-12 v2.10
  * Initial release of golden morphologically annoated corpus

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.10
License: CC BY-NC-SA 3.0
Includes text: yes
Genre: news grammar-examples poetry fiction
Lemmas: automatic with corrections
UPOS: automatic with corrections
XPOS: not available
Features: automatic with corrections
Relations: converted from manual
Contributors: Karahóǧa, Ritván; Stamou, Vivian; Markantonatou, Stella
Contributing: elsewhere
Contact: marks@athenarc.gr
===============================================================================
</pre>
