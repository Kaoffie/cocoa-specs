## Cocoa Theory Specifications

This is a documentation for Cocoa Theory, a stenographic theory for writing English on the Ward Stone Ireland layout. 

This document will seem very complicated to a lot of learners, but it is important to note that large portions of the text in this document have been dedicated to explaining very rare corner cases in the theory, most of which users will rarely encounter.

Hence, it should not be used as a primary learning resource. Users are still welcome to use this document as an additional reference document to look up on any additional details that may be missing in other resources.

### Explanation of Badges

Throughout the document, badges have been added to various topics to indicate their development progress. They are as follows:

| Badges |
|---|
| ![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=) <br> All details have been fully documented and are not likely to change in the future. |
| ![](https://img.shields.io/badge/-to%20be%20documented-yellow?style=for-the-badge&logo=) <br> Details have been sorted out and are waiting to be documented. |
| ![](https://img.shields.io/badge/-to%20be%20expanded-blue?style=for-the-badge&logo=) <br> Details have only been partially documented and will be expanded in the future. |
| ![](https://img.shields.io/badge/-work%20in%20progress-orange?style=for-the-badge&logo=) <br> Currently being worked on. Any details that have been recorded are not final. |
| ![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=) <br> Will very likely change in the future. |

### Table of Contents

- [Cocoa Theory Specifications](#cocoa-theory-specifications)
  - [Explanation of Badges](#explanation-of-badges)
  - [Table of Contents](#table-of-contents)
- [Design Objectives](#design-objectives)
  - [Technical Objectives](#technical-objectives)
  - [What Cocoa Theory is not](#what-cocoa-theory-is-not)
- [Fingerspelling](#fingerspelling)
  - [Fingerspelling Alphabet](#fingerspelling-alphabet)
  - [Fingerspelling Variants](#fingerspelling-variants)
- [Initials](#initials)
  - [Phonetic Initials](#phonetic-initials)
  - [Consonant Clusters](#consonant-clusters)
  - [Overloaded Initials](#overloaded-initials)
  - [Orthographic Initials](#orthographic-initials)
  - [Advanced Initials](#advanced-initials)
  - [Initial Joiners](#initial-joiners)
  - [T and D](#t-and-d)
- [Medials (Vowels)](#medials-vowels)
  - [Orthographic Overrides](#orthographic-overrides)
  - [Short Vowels](#short-vowels)
  - [Long Vowels](#long-vowels)
  - [Vowels before R](#vowels-before-r)
  - [Exceptions for a~e and o~e](#exceptions-for-ae-and-oe)
  - [Disambiguators in Conjugated Words](#disambiguators-in-conjugated-words)
  - [Compressed Glides](#compressed-glides)
  - [Compressed AOEU Triphthongs](#compressed-aoeu-triphthongs)
  - [OE and AOE](#oe-and-aoe)
  - [OEU Briefing](#oeu-briefing)
- [Finals](#finals)
  - [Orthographic Overrides](#orthographic-overrides-1)
  - [Phonetic Finals](#phonetic-finals)
  - [Final Inversion](#final-inversion)
  - [Orthographic Disambiguators](#orthographic-disambiguators)
  - [T and D](#t-and-d-1)
  - [Folded Suffixes](#folded-suffixes)
  - [`-F` as S](#-f-as-s)
  - [`-FR` as M](#-fr-as-m)
  - [Asterisk Dropping in V and Z](#asterisk-dropping-in-v-and-z)
  - [Advanced finals](#advanced-finals)
- [Syllable Splitting](#syllable-splitting)
  - [Right Greedy Splitting](#right-greedy-splitting)
  - [Dividing Clusters](#dividing-clusters)
  - [Left Bank Glides](#left-bank-glides)
  - [Syllable/Stroke Dropping](#syllablestroke-dropping)
  - [Consonant Greedy](#consonant-greedy)
  - [-y Suffix](#-y-suffix)
- [Edge Cases](#edge-cases)
  - [Silent Finals in French Loanwords](#silent-finals-in-french-loanwords)
  - [Greek and Latin Plurals](#greek-and-latin-plurals)
- [Common briefs](#common-briefs)
- [Numbers](#numbers)
  - [Single Digits & Trailing Zeros](#single-digits--trailing-zeros)
  - [Two-digit and Three-digit Numbers](#two-digit-and-three-digit-numbers)
  - [Number modifiers](#number-modifiers)
- [Symbols](#symbols)
  - [Punctuation](#punctuation)
  - [Diacritics](#diacritics)
- [Formatting](#formatting)
- [Modifiers](#modifiers)
- [Orthographic System](#orthographic-system)
  - [Initials](#initials-1)
  - [Medials](#medials)
  - [Finals](#finals-1)
- [Phrasing System](#phrasing-system)

## Design Objectives

Cocoa Theory is derived from Plover Theory, with heavy influences from Phoenix and Realwrite/Realtime, as well as theory ideas floating around on the Plover Discord. It is a mixed (phonetic-orthographic) theory with heavy use of orthographic disambiguation. It was initially created as a variant of Plover Theory to fix three major problems with the theory: Reliance on stress-based syllable dropping, lack of consistency in syllable splitting, and the overuse of disambiguation by asterisks. Since then, it has undergone enough changes to be considered an independent theory. The main design goals are:

- To provide a theory designed for everyday use in mind, rather than court reporting and captioning;
- to remove dependence on stress-based syllable dropping, as not all English speakers are capable of identifying stressed and unstressed syllables. This does not indicate the complete removal of stress-based syllable dropping, but merely makes it optional;
- to provide spelling-based disambiguation for all the major conflict-prone medials;
- to accomodate for short writing styles, including folding and phrasing, whilst not making it compulsory;
- to make the outlines of all words predictable, even if their pronunciation is unknown, using a systematic syllable splitting standard;
- to support British spellings using orthographic disambiguation;
- to reduce the amount of memorization as much as possible by reducing the reliance on special affix strokes, the number of mandatories, and frequency-based disambiguation.

### Technical Objectives

There are a few technical goals that the theory tends to stick to when introducing new rules:

- Not to make Philly shifting compulsory; users are still free to implement them in their own writing if they like it, but it should not be necessary.
- Asterisks should only be used phonetically for finals. 

### What Cocoa Theory is not

Cocoa Theory is not an orthographic theory.

It is a mixed system, based partially on the General American accent, but with more leniency for other accents and alternative pronunciations. If the user's accent is generally mutually intelligible with American English, which covers most major English speaking regions as well as most English learners, then this thoery should work for them. 

During the design process, the following points were considered:

- **Non-rhotic accents**: Not including R sounds would make the theory more unfriendly to other speakers; as such, speakers with non-rhotic accents should expect to include unprounounced R sounds in their writing, such as the R in "hour", "bar", "hear", etc. This includes most English (British), Welsh, Australian, New Zealand, and Singaporean/Malaysian accents, as well as some accents in India, Pakistan, and the American South.
- **Syllable-timed/Mora-timed accents**: There are both native speakers and learners who speak accents with reduced stress patterns or with no stressed/unstressed syllables. Much like many traditional theories, Cocoa Theory takes advantage of stress patterns to drop syllables to write shorter; this, however, is completely optional, and stress is not required for writing. This should make it much easier for East or Southeast Asian speakers, or native speakers of non-stress-timed languages such as French, Italian, or Spanish (just to list a few).
- **Reduced vowels and schwas**: Vowel reduction is not consistent across accents. Cocoa Theory attempts to provide the non-reduced outlines wherever possible, extrapolated based on spelling. For instance, "considerate" does not rhyme with "crate" due to the final syllable being a schwa, but there will be a dictionary entry that fits the prounuciation where they do rhyme.

However, if the user's accent or dialect deviates too much (to the point where vowel lexical sets fail to capture their accent), then they may run into a few obstacles with this theory. This does not mean that they should not use this theory - this merely means that they should expect to make a lot more changes to their personal dictionary than the average user. In other words, if their accent is "heavy" enough that other speakers from other regions may have difficulty understanding them, then they may have to use a lot more custom dictionary entries that fit your pronunciation.

## Fingerspelling

### Fingerspelling Alphabet

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Fingerspelling is done with the left hand, with the right hand in charge of spelling variants. The letters are as follows:

| Letter | Chord | Letter | Chord |
|---:|:---|---:|:---|
| a | `A` | n | `TPH` |
| b | `PW` | o | `O` |
| c | `KPW` or `KR` | p | `P` |
| d | `TK` | q | `KW` |
| e | `E` | r | `R` |
| f | `TP` | s | `S` |
| g | `TKPW` | t | `T` |
| h | `H` | u | `U` |
| i | `EU` | v | `SR` |
| j | `SKWR` | w | `W` |
| k | `K` | x | `SKPH` or `KP` |
| l | `HR` | y | `KWR` |
| m | `PH` | z | `SKW` |

### Fingerspelling Variants

![](https://img.shields.io/badge/-to%20be%20expanded-blue?style=for-the-badge&logo=)

The variants are as follows: (Subject to change)

| Variant | Example | Chord |
|---:|:---:|:---|
| Lowercase | abc | `*` |
| Uppercase | ABC | `*P` |
| Lowercase stitching | a-b-c | `-RBGZ` |
| Uppercase stitching | A-B-C | `-FPLD` |
| Lowercase dotted | a.b.c. | `-RBLS` |
| Uppercase dotted | A.B.C. | `-RPGS` |
| Unused | | `*RBGZ` |
| Unused | | `*FPLD` |
| Unused | | `*RBLS` |
| Unused | | `*RPGS` |

## Initials

Initials in Cocoa Theory are written using the left bank keys (`STKPWHR`). Whilst the vast majority of words can be written phonetically, many are written orthographically instead to resolve conflicts in what could be considered a mixed system. In general, however, we can expect silent letters to be ignored, unless specified in the following sections. For instance:

- "p" in "pneumatic": `TPHAOUPL/SWRAT/SWREUBG` (nuum-at-ik)
- "w" in "answer": `APBS/SWRER` (ans-er)

Most rules are inherited from Plover Theory, but some chords have been changed to avoid conflicts. In situations where there is an orthographic disambiguation initial chord for a word that does not require conflict resolution, we offer both the phonetic and orthographic variants and leave it to the user to decide which to use.

### Phonetic Initials

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

These are all the initials that are written phonetically:

| Final | Chord | Final | Chord |
|---:|:---|---:|:---|
| /b/ | `PW` | /t/ | `T` |
| /d/ | `TK` | /v/ | `SR` |
| /f/ | `TP` | /w/ | `W` |
| /ɡ/ | `TKPW` | /ks/ | `SKPH` |
| /h/ | `H` | /j/ | `KWR` |
| /dʒ/ | `SKWR` | /z/ | `SKW` |
| /k/ | `K` | /ʃ/ | `SH` |
| /l/ | `HR` | /tʃ/ | `KH` |
| /m/ | `PH` | /θ/ | `TH` |
| /n/ | `TPH` | /ð/ | `TH` |
| /p/ | `P` | /ʒ/ | `SKWR` |
| /kw/ | `KW` | /ʃɹ/ | `SKHR` |
| /ɹ/ | `R` | /tʃʊ/ | `TW` |
| /s/ | `S` | | |

### Consonant Clusters

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Initial consonant clusters are built using the basic initial sounds, and in most instances can be chained together without breaking steno order. For instance:

- Initial /fl/: `TPHR`
- Initial /bɹ/: `PWR`
- Initial /skɹ/: `SKR`

There are, however, instances where we are forced to break steno order to accomodate rare initial consonant clusters. We do this by stacking or using inversion; note that in the case of stacking, the individual sub-chords that are stacked together do not overlap. Note that "kn" is not considered a cluster since it is a single sound. 

- Initial /θw/: `TWH`
- Initial /nj/: `TKPWHR`

In the case of glides, /j/ and /w/ in particular, whilst they can be represented sometimes with a stacked `KWR` and `W` respectively, if the glide is included as part of the vowel, such as `AOU` /juː/, then they should not be stacked. For example, the first syllable of "music" is represented with `PHAOUS`, not `KPWHRAOUS` or `KPWHRUS`.

Overlapped stacking is only used when there is no other choice, such as when a word begins with the consonant cluster in question and the first chord has to include the entire cluster. 

- Initial /lm/, /ml/: `PHR`
- Initial /vl/: `SHR`

### Overloaded Initials

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Some existing initials also have additional functions:

- `S-` can be used as a vowel wildcard
- `W-` can be used for "V" sounds
- `H-` can be used for "W" or "U" sounds when `W` is taken
- `TPH-` can be used for "in-", "en-", "on-"
- `HR-` can be used for "el-", "al-"
- `SKPH-` can be used for "exc-"

These additional functions can be combined with inversion and stacking:

- Initial /ɡw/: `TKPWH`
- Initial /bw/: `PWH`

Some initials that include the /ʃ/ sound cannot be properly accomodated on the layout, and are represented by just the `S-` key. However, when the option to stack consonants regardless of steno order is available, we stack the sounds instead:

- Initial /ʃl/: `SHR`
- Initial /ʃm/: `SPH`
- Initial /ʃt/: `STH`
- Initial /ʃw/: `SWH`

Note that this does not apply to qu-, which is stroked with `KW`, not `KWH`.

### Orthographic Initials

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Whilst most initials are written phonetically, a few exceptions exist due to the need for disambiguation:

| Initial | Chord | Remarks |
|---:|:---|:---|
| c | `KPW` | Only when pronounced as /s/ |
| wh | `WH` | Note that some speakers do pronounce wh- differently from w- |
| wr | `WR` | Note that some speakers do pronounce wr- differently from r- |
| tw | `TW` | Only when pronounced as /t/. This is specifically for derivatives of "two". |
| ch | `KH` | Only when pronounced as /k/ or /ʃ/ |
| sc | `SKPH` | Only when pronounced as /s/ |
| sch | `SKH` | Only when pronounced as /ʃ/ |
| kn | `TKPH` | |
| ph | `TKP` | |

In cases where disambiguation is not necessary, such as "knife", both the phonetic (`TPHAOEUF`) and the orthographic stroke (`TKPHAOEUF`) should be provided, chosen by the user based on preference. 

There are also many cases where we include the orthographic entry not for disambiguation, but to anticipate situations where the speaker actually pronounces these words based on how they are spelled, unaware of the exceptions in English orthography. 

Note that initial gh- is written as `TKPW`, not `TKPWH`. The latter chord may be used for disambiguation if necessary, but I have not come across any situations where I have required it so far. Hence the following words are written with `TKPW`:

- gherkin: `TKPWERBG/SWREUPB`, not `TKPWHERBG/SWREUPB`
- ghetto: `TKPWET/SWROE`, not `TKPWHET/SWROE`

Nevertheless, there isn't actually anything bad with the chord `TKPWH`, so the user can add it for words starting with gh- if they so choose to.

### Advanced Initials

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

These initials are either memorized or constructed from the principles listed previously, but they are mostly used in briefs rather than syllable-based outlines.

| Initial | Pronunciations | Chord | Remarks |
|---:|:---|:---|:---|
| des, dis | /dɪs/ | `STK` | |
| exp, and, end | /ɪksp/, /ænd/, /ɛnd/ | `SKP` | |
| imp, emp | /ɪmp/, /ɛmp/ | `STKPW` | |
| int, ent | /ɪnt/, /ənt/, /ɛnt/, /ɑnt/ | `SPW` | |
| ext | /ɪkst/, /ɛkst/ | `SKPW` | |
| inf | /ɪnf/ | `STKPH` | |
| adv | /ædv/, /ədv/ | `STKW` | |
| inv | /ɪnv/ | `STPHR` | |
| ins, ens, inst | /ɪns/, /ɛns/, /ɑns/, /ɪnst/ | `STPH` | |
| rev, riv, rew, rw | /ɹəv/, /ɹɪv/, /ɹəw/, /ɹɪw/ | `WR` | |

### Initial Joiners

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

There are also two joiners, used to indicate the lack of an initial consonant sound. These are explained in the syllable splitting section.

- Generic initial joiner: `SWH`
- Orthographic joiner: `KWH`

Since `KWH` is reserved as the orthographic joiner, we cannot use it for the chw- sound, present in words such as "factual" or "eventually". As mentioned previously, that sound uses the `TW` chord instead - if necessary, this can be seen as an orthographic chord. 

### T and D

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

The letters "t" and "d" are often pronounced as /tʃ/ and /dʒ/, especially in the UK, such as in "Tuesday" /ˈt͡ʃuːzdeɪ/ or "during" /ˈdʒʊəɹɪŋ/. At the beginning of words, they are stroked orthographically, using `T` or `TK`:

- Tuesday: `TAO*UZ/SWRAEUFB`
- during: `TKAOUR/-G`

However, they can be written phonetically when they occur elsewhere. This should not be relied upon, and the dictionary will not include every entry, only the ones that are pronounced this way in General American accents:

- capture: `KAP/SKHUR` (kap-chur) or `KAPT/SWRAOUR` (kapt-uur) or `KAPT/SWRUR` (kapt-ur)
- culture: `KUL/SKHUR` (kul-chur) or `KULT/SWRAOUR` (kult-uur) or `KULT/SWRUR` (kult-ur)
- presumptuous: `PRES/SWRUFRP/SKHU/SWROUS` (pres-ump-chu-ous) or `PRES/SWRUFRPT/SWOUS` (pres-umpt-uous)

The same letters "t" and "d" are also often pronounced as /ɾ/, like in "little" or "paddle". Due to syllable splitting, these usually do not happen in the initial, but in cases where they do, they are exclusively written orthographically as `T` and `TK` respectively.

## Medials (Vowels)

Vowels are written using the thumb keys `AOEU`. Vowels in English are a mess, so whilst the system has inherited most of the phonetic vowel chords from Plover Theory, it leans towards the orthographic side, with many orthographic disambiguators recommended for use even if there are no conflicts. 

Many of these disambiguators overlap with final chords, especially `-FB` and `-PZ`. They will be mentioned briefly in this section, and will be explained again in the finals section.

The vowel system is rhotic, to avoid conflicts. For speakers who have a non-rhotic accent, it may be helpful to view it from an orthographic point of view.

### Orthographic Overrides

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

If any vowel clusters are spelled with the following sequences of letters, then they are stroked orthographically regardless of pronunciation:

| Spelling | Chord |
|---:|:---|
| ai | `AEU` |
| au | `AU` |
| ae, ea | `AE` |
| ea | `AE` |
| oo, ao | `AO` |
| oa | `OE` |
| aou, oau | `AOU` |
| ou | `OU` |

There are instances where we find these spellings in vowel clusters that would be considered as two syllables, such as the "oo" in coordination. In these cases, we can apply the orthographic overrides as usual, or split it into two syllables. Some examples include:

- "oo" in "coordination": `KAORD/SWREUPB/SWRAEUGS` or `KOE/SWRORD/SWREUPB/SWRAEUGS` or `KO/SWRORD/SWREUPB/SWRAEUGS`
- "ea" in "reality": `RAEL/SWREUT/KWREU` or `RAOE/SWRAL/SWREUT/KWREU` or `RE/SWRAL/SWREUT/KWREU`

There are also instances where we find these spellings as part of a longer string of vowels. We will still write them with the orthographic override. If a string contains multiple orthographic overrides, follow the rightmost one. Since these words tend to be rarer and are typically loanwords, we can afford to be more lenient with them.

### Short Vowels

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

The precise definition of a "short" vowel in this context is any of the vowels listed below. Many of them are merged in many dialects. They are generally stroked based on spelling.

| Lexical Set | Examples | Fallback |
|---:|:---|:---|
| kit | ship `SHEUP`, myth `PH*EUT` | `EU` |
| dress | step `STEP`, ready `RAED/KWREU` | `E` |
| trap | bad `PWAD`, cab `KAB` | `A` |
| lot | stop `STOP`, job `SKWROB` | `O` |
| strut | cup `KUP`, budge `PWUPBLG` | `U` |
| bath | staff `STAF`, dance `TKAPBS` | `A` |
| palm | balm `PWAUPL`, sergeant `SERPBLG/SWRAEPBT` | `A` |
| cloth | cough `KOUF`, broth `PWRO*T` | `O` |
| foot | put `PUT`, look `HRAOBG` | `U` |
| comma (schwa) | around `AR/SWROUPBD`, vodka `SROD/SKA` | Final vowel letter (including y) |

Spellings of vowels are usually converted into steno like so:

| Spelling | Chord | Remarks |
|---:|:---|:---|
| ai | `AEU` | Orthographic Override |
| au | `AU` | Orthographic Override |
| ae, ea | `AE` | Orthographic Override |
| ea | `AE` | Orthographic Override |
| oo, ao | `AO` | Orthographic Override |
| oa | `OE` | Orthographic Override |
| aou, oau | `AOU` | Orthographic Override |
| ou | `OU` | Orthographic Override |
| a | `A` | |
| e | `E` | |
| i, y | `EU` | |
| o | `O` | |
| u | `U` | |
| w | `AOU` | Only when used as a vowel; see below |

Some vowel sounds require us to write with spelling. In some cases, the letters "y" and "w" may be used to spell those vowels. In those cases, we use the chords `EU` and `AOU` to represent them respectively. For instance:

- "y" in myth: `PH*EUT`
- "w" in crwth: `KRAO*UT`

We will often find words that cannot be stroked by spelling, because the combination of letters used to represent the vowel is too rare to warrant a special chord. In this case, we stroke them phonetically, using the fallback column. If the fallback column is empty, then we take the rightmost vowel. Here are some examples of the fallback column in use:

- "ie" in "friend": `TPREPBD`
- "ue" in "conquer": `KOFRPBG/SWRER`

When the spelling of a word deviates too much from its spelling, we will also offer a phonetic outline, using the fallback chord associated with the vowel. For instance:

- "u" in "minute": `PHEUPB/SWREUT`
- "u" in "busy": `PWEUS/KWREU`, `PWEUZ/KWREU`
- "o" in "women": `WEUPL/SWREPB`

For the palm vowel specifically, whenever the vowel is spelled as "au", "al", or "aw", we use `AU` instead of `A`, as with the outline listed for "balm". 

### Long Vowels

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Long vowels are all vowels that aren't short, including diphthongs. All of them have a base chord, but since conflict rates are often high, they all have a list of associated disambiguators, each corresponding to a possible spelling of the vowel.

~ is a consonant wildcard. Note that orthographic overrides take priority.

| Lexical Set | Base Chord | Disambiguators |
|---:|:---|:---|
| fleece | `AOE` | i `EU` |
| face | `AEU` | ei `AE`, ey `EFB`, ay `AEUFB`, a~e `AEF` |
| goat | `OE` | o `O`, ow `OEFB`, o~e `OEF` |
| thought | `O` | aw `AUFB`, ow `OUFB` |
| goose | `AOU` | o `O`, u `AOU`, ew `AOUFB`, o~e `OE` |
| price | `AOEU` | y `AOEUFB`, uy `UFB`, ye `AOEUFB`|
| choice | `OEU` | oy `OEUFB` |
| mouth | `OU` | ow `OUFB` |

Note that we have placed the thought vowel in the long vowel category and the lot vowel in the short category. To combat the cot-caught merger, they have been allocated the same base chord. 

If we encounter a long vowel with spelling that is not included in the list of disambiguators, we can safely stroke it using the base chord. For instance:

- "ai" in "maid": `PHAEUD`
- "oe" in "roe": `ROE`

Whenever we use `AOU`, we can safely include glided Y sounds into the vowel, instead of deferring them to the initial or the previous chord:

- "iew" in "view": `SRAOUFB`

Since many of the disambiguators include keys from the right bank, they can sometimes interfere with the final consonants in a given stroke. In cases where the keys do not overlap, we can safely include the entire disambiguator, even if steno order is broken:

- "ow" in "bowl": `PWOEFBL`
- "ow" in "power": `POUFRB` or `POUFB/SWRER`
- "a(t)e" in "rate": `RAEFT`
- "a(th)e" in "bathe" `PWA*EFT`

There are cases, however, where they overlap. In these cases, we can continue using the disambiguators, but without the right bank keys. For instance:

- "ow" in "down": `TKOUPB`
- "aw" in "pawn": `PAUPB`
- "a~e" in "pave": `PA*EF`
- "a~e" in "safe": `SAEF`

It is important to note that the phonetic outlines, based on the base chords in the table above, will still be provided when there are no conflicts to disambiguate.

### Vowels before R

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Rhotic vowels generally follow the same rules as the two categories above, but with an additional `-R` added at the back.

| Lexical Set | Examples | Fallback |
|---:|:---|:---|
| nurse | hurt `HURT`, term `TERPL` | - |
| start | heart `HAERT`, carve `KAFRB` | `AR` |
| north | short `SHORT`, war `WAR` | - |
| force | four `TPOUR`, spore `SPOR` | `OR` |
| letter | meter `PHAOET/SWRER`, metre `PHAOET/SWR-R` | - |

Note that "er" is stroked as `ER`, but "re" (commonly used in British spelling) is stroked as just `-R`. This allows us to write both American and British spellings.

| Lexical Set | Base Chord | Disambiguators |
|---:|:---|:---|
| near | `AOER` | |
| square | `AEUR` | are `AEFR` |
| cure | `AOUR` | |

Naturally, the phonetic outlines will still be available for many of these words, and will be recommended when users are not used to this system.

### Exceptions for a~e and o~e

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

The "a~e" pattern for "face" vowels is stroked as `AEF`, like so:

- base: `PWAEFS`
- rate: `RAEFT`
- taste: `TA*EFS`
- fame: `TPAEFPL`

Whist the "o~e" pattern for "goat" vowels is similarly stroked as `OEF`, like so:

- prose: `PROEFS`
- home: `HOEFPL`
- swole: `SWOEFL`

Note that clusters containing multiple consonants can also be matched with the "~" wildcard. 

This is mainly to avoid conflicts with the "ai" vowel spelling, which often is pronounced the same way. However, there is one single exception to this rule - when used with `-P`, this can conflict with any syllables ending with "-each" or "-oach", such as "teach"/"tape" or "coach"/"cope". Thus for /p/ specifically, we will stick to the base chord:

- tape: `TAEUP`
- cope: `KOEP`

Note that the `AEF` pattern does not apply to other similar patterns with a silent "e". "praise", for instance, is not spelled with the "a~e" pattern due to the extra "i". Its outline is hence `PRAEUS`, using the base vowel chord `AEU`, rather than `PRAEFS` or `PRAEUFS`, influenced by the silent "e".

### Disambiguators in Conjugated Words

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

When words are conjugated or modified with affixes, the vowel strings that determine which chord or disambiguator we use may change. In these instances, we can choose to use either the original chord, or to ignore it and construct the outline based on the new modified spelling:

- bellies: `PWEL/SWREU/-S` or `PWEL/KWREU/-S`
- casing: `KAEFS/-G` or `KAEUS/-G`

### Compressed Glides

![](https://img.shields.io/badge/-to%20be%20documented-yellow?style=for-the-badge&logo=)

### Compressed AOEU Triphthongs

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Triphthongs that contain the price vowel can often be compressed into a single stroke with the `AOEU` chord, instead of being split into two strokes. For instance:

- iron: `AOEURPB`
- denial: `TKEPB/SWRAOEUL`

### OE and AOE

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

When long vowels are written with a single letter, some users may find it difficult to use the actual long vowel chord rather than the single letter key/chord corresponding to the letter. Cocoa Theory tries to account for this specifically for the goat vowel by including both the orthographic and phonetic variants:

- "o" in "macho": `O` or `OE`

Another problem is when a word starts with an e-, which can either be pronounced as the fleece vowel, or as a reduced schwa. Again, both variants would be included:

- "e" in "ecology": `E` or `AOE`

### OEU Briefing

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

The `OEU` chord is also sometimes used for one of two things:

- To indicate that there is an additional -y after the current syllable, such as in "happy". Whilst Plover Theory also uses `AE` for this purpose, Cocoa only uses `OEU`, and applies it to a much smaller selection of words. (TBC: Experiment with `-DZ` for final -y, or some other pinky chord)

- As a wildcard, to provide an alternative to skeletal briefs.

These two uses should not be treated as consistent rules, but rather as briefing techniques.

## Finals

Whilst finals are mostly stroked phonetically, there are too many orthographic finals that it would be odd to call it phonetic. With that in mind, due to the syllable splitting used in the theory, finals play an extremely important role in representing complex consonant clusters, much more complex than on the left bank (appropriate given that the right bank has more keys).

Still, similar to initials, we can expect most silent letters to be ignored, unless any of the following sections say otherwise. Also similar to initials, if there is an orthographic disambiguator available for a given final, but no conflict is present, both the phonetic and orthographic outlines should be offered.

### Orthographic Overrides

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

These orthographic override finals apply whenever the spelling matches one of the endings specified below. They exist due to confusion about their exact pronunciation, or in the case of -x, for conflict resolution.

| Ending | Chord | Remarks |
|---:|:---|:---|
| mb | `-FRB` | `-FR` as "m" |
| mn | `-FRPB` | `-FR` as "m" |
| x | `*BGS` | |
| s | `-S` | |
| t | `-T` | |
| st, zt | `*S` | |
| sd, zd | `*Z` | |

The letters "s" is often pronounced as a /z/ sound in the finals. This can be extremely confusing for many English speakers, even though it is second nature to some. To reduce confusion, whenever a final is spelled with an "s", there will be an outline for it that uses `-S`. If it is pronounced as /z/ and there are no conflicts, then the `-Z` outline would also be provided. 

The "t" sound is similar - it may sometimes be pronounced as a /d/, but will always be stroked as `-T`.

This merger does lead to new conflicts that need to be resolved; however, we will not use `-S` and `-Z` to resolve them, and will instead resort to other disambiguation methods:

| Word | Plover | Cocoa |
|---:|:---|:---|
| race | `RAEUS` | `RAEFS` |
| raise | `RAEUZ` | `RAEUS` or `RAEUZ` | 
| brace | `PWRAEUS` | `PWRAEFS` |
| braise | `PWRAEUZ` | `PWRAEUS` or `PWRAEUZ` | 

### Phonetic Finals

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Those familiar with English phonotactics will recognize a few sounds in the table below that don't go at the end of English syllables. They are included as finals as a side effect of greedy syllable splitting.

| Final | Chord | Final | Chord |
|---:|:---|---:|:---|
| /b/ | `-B` | /ɹ/ | `-R` |
| /d/ | `-D` | /v/ | `*F` |
| /f/ | `-F` | /w/ | `-FB` |
| /ɡ/ | `-G` | /z/ | `-Z` |
| /h/ | `-PZ` | /dʒ/ | `-PBLG` |
| /k/ | `-BG` | /ʃ/ | `-RB` |
| /l/ | `-L` | /tʃ/ | `-FP` |
| /m/ | `-PL` | /θ/ | `*T*` |
| /n/ | `-PB` | /ð/ | `*T` |
| /p/ | `-P` | /ŋ/ | `-PBG` |

Most consonant clusters that are composed with sequences of sounds from the chart above can also be similarly composed in steno by ordering the sounds in steno order. 

Some clusters, however, need to be handled differently:

| Cluster | Chord | Remarks |
|---:|:---|:---|
| /kst/ | `-GT` | |
| /ksd/ | `-GD` | |
| /ldʒ/ | `-LG` | |
| /nk/, /ŋk/ | `-FRPBG` | |
| /ntʃ/ | `-FRPB` | |
| /ɹtʃ/ | `*FRPB` | TBC: Currently being tested |
| /ltʃ/ | `-LG` | |
| /nʃ/ | `-PBZ` | TBC: Currently being tested |
| /ɹʃ/ | `-RZ` | TBC: Currently being tested |
| /lʃ/ | `-LZ` | TBC: Currently being tested |
| /ɹb/ | `*RB` | Prevent conflicts with -sh |
| /ɹv/ | `-FRB` | |
| /lk/ | `*LG` | |
| /lp/ | `-P` | /l/ is ignored. |
| /lm/ | `-PL` | /l/ is ignored. In many cases, the "l" is accounted for as part of the vowel, such as "calm" `KAUPL` |

When arranging chords in steno order, we can safely ignore asterisks. For instance, /ɹst/ is `*RS`, since we can ignore the asterisk in `*S` and consider `*S` as a chord that comes after `-R`. 

### Final Inversion

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

In some instances, we cannot arrange the chords we need in steno order to completely represent a consonant cluster. Normally, this forces us to split the cluster into two, even if we are dealing with the last syllable of the word. However, in some cases, we can use inversion to reduce the total number of strokes. This is mostly optional.

| Cluster | Final Syllable | Non-final Syllable | With Inversion |
|---:|:---|:---|:---|
| /ɹf/ | `-R/SWR-F` | `-R/TP...` | `-FR` |
| /lf/ | `-L/SWR-F` | `-L/TP...` | `-FL` |
| /lv/ | `-L/SWR*F` | `-L/SR...` | `*FL` |
| /dθ/ | `-D/SWR*T` | `-D/TH...` | `*TD` |
| /lb/ | `-L/SWR-B` | `-L/PW...` | `-BL` |

There are two inversion cases that are treated differently to avoid conflicts:

| Cluster | Without Inversion | With Inversion |
|---:|:---|:---|
| tle | `-T/SWR-L` | `*LT` |
| dle | `-D/SWR-L` | `*LD` |

### Orthographic Disambiguators

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

There are two cases where the pronunciation of a final is not enough to determine what chord to use:

| Final | Remarks |
|---:|:---|
| /ʒ/ | If spelled with any sequence containing "s", use `-RB`. Otherwise, use `-PBLG`. |
| /ks/ | If spelled as "x", use `*BGS`. Otherwise, treat it as /k/ + /s/ and write `-BGS`. |

There is also a small selection of orthographic disambiguators. `-FB` has already been covered in the vowels section, but they will be mentioned again here:

| Final | Disambiguator Chord |
|---:|:---|
| Silent h, gh | `-PZ` |
| ght | `-GT` |
| w, y | `-FB` (For details on usage, see vowels.) |

For instance:

- hi: `HAOEU`
- high: `HAOEUPZ`
- lite: `HRAOEUT`
- light: `HRAOEUGT`

### T and D

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

As stated before, the letters "t" and "d" are often pronounced as /tʃ/ and /dʒ/. In these cases, they should be stroked orthographically, as it can be rather difficult to predict when such pronunciations occur. However, they can be stroked phonetically sometimes, based on the General American accent:

- nature: `NAEUT/SWRAOUR` or `NAEUT/SWRUR` or `NAEUFP/SWRAOUR` or `NAEUFP/SWRUR`
- graduate (verb): `TKPWRAD/SWAEFT` or `TKPWRAPBLG/SWAEFT`

Users are recommended to either use the orthographic outlines, or to define their own phonetic outlines to fill in the gaps of the dictionary based on their personal preferences.

### Folded Suffixes

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

There are a few folded suffixes supported by Plover:

| Suffixes | Chords | Remarks |
|---:|:---|:---|
| ing | `-G` | When briefing, we can use `-DZ` when `-G` is not available. |
| d, ed | `-D` | When briefing, we can use `-TD` for "-ded". |
| s, es | `-S`, `-Z` | Depends on which one is easier to press (`-TS` vs `-DZ`) |

It is generally recommended to write these suffixes separately to avoid conflicts, but with sufficient familiarity with one's own dictionary, they can be folded.

Additionally, there are a few suffixes that can be "folded", but must be defined explicitly in the dictionary. They are optional and mostly used in briefs.

| Suffixes | Chords | Remarks |
|---:|:---|:---|
| re, er | `-R` | Conflict-prone, use with caution |
| al, ly | `-L` | Conflict-prone, use with caution |

In the case of "al" or "ly", if `-L` is not available, the left bank chord `HR` can be used instead, even if it means overlapping chords on the left bank. For instance:

- finally: `TPHRAOEUPBL`
- normally: `TPHROFRL`

### `-F` as S

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

In some cases, we need to write the letter "s" before another consonant; this is made difficult by the fact that the `-S` key is near the end of steno order. In these cases, we can use `-F` to represent "s" instead. Here are some examples:

| Cluster | Chord |
|---:|:---|
| "s" + /p/ | `-FP` |
| "s" + /k/ | `-FBG` |
| "s" + /m/ | `-FPL` |
| "s" + /l/ | `-FL` |

Note that "st" is not `-FT`, but `*S`. This is to avoid conflicts.

By adding an asterisk, we can represent the letter "z" as well, though this is much less common:

| Cluster | Chord |
|---:|:---|
| "z" + /p/ | `*FP` |
| "z" + /k/ | `*FBG` |
| "z" + /m/ | `*FPL` |
| "z" + /l/ | `*FL` |

Another use case of `-F` is for the "-sing" final, where we need to combine a final "s" with a folded "-ing" suffix. Instead of using `-GS`, we can use `-FG` instead. This, however, is not encouraged, due to the increased conflict rates. Beginners are still recommended to write `-G` as a separate stroke, unless they are familiar enough with their own dictionary to know when `-FG` will give them the right output.

### `-FR` as M

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Similar to how `-F` can represent "s", we can use `-FR` to represent the /m/ sound whenever we cannot represent a cluster that contains the sound properly using steno order without overlapping. For instance:

| Cluster | Chord | Remarks |
|---:|:---|:---|
| /mp/ | `-FRP` | |
| /mk/ | `-FRBG` | |
| /mn/ | `-FRPB` | |
| /ml/ | `-FRL` | |
| /mb/ | `-FRB` | There are instances where the "b" in "mb" is silent, but this can be difficult to predict. Hence `-FRB` is used to represent "mb" in all instances as an orthographic override, rather than a phonetic chord. |

### Asterisk Dropping in V and Z

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

For convenience, the asterisk in `*F` used to represent /v/ can be dropped whenever there are no conflicts. For instance:

- rave: `RAEF` or `RA*EF`
- save: `SA*EF`, but not `SAEF` due to conflict with "safe"

This can also apply to instances where `*F` is used to represent "z":

- freezer: `TPRAOEFR` or `TPRAO*EFR`
- razer: `RA*EUFR`, but not `RAEUFR` due to conflict with "racer"

### Advanced finals

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

There are also a few finals that represent an entire syllable; they are used in write-outs and should be taught fairly early on, but are optional.

| Final | Chord | Syllable Replacement | Remarks |
|---:|:---|:---|:---|
| /bəl/ | `-BL` | Yes | |
| /pəl/ | `-PL` | - | |
| /fəl/, /fuːl/ | `-FL` | Yes | |
| /vəl/, /zəl/ | `*FL` | - | Subject to asterisk dropping. |
| /təl/ | `*LT` | - | See section above on Final Inversions. |
| /dəl/ | `*LD` | - | Same as above. |
| /fəɹ/, /ðəɹ/ | `-FR` | - | |
| /vəɹ/ | `*FR` | - | Subject to V asterisk dropping. |
| /ʒəɹ/ | `*FR` | - | Asterisk cannot be dropped. (TBC) |
| /mənt/ | `-PLT` | Yes | |
| /nəs/, /nɪs/ | `-PBS` | Yes | |
| /ʃən/, /ʒən/, /dʒən/ | `-GS` | Yes | |
| /nʃən/, /neɪʃən/ | `-PBGS` | - | Also applies to any of the -shun variants above. |
| /kʃən/, /keɪʃən/ | `-BGS` | - | Same as above. |
| /lʃən/, /luːʃən/, /luːʒən/ | `-LGS` | - | Same as above. |
| /ŋkʃən/ | `-FRPBGS` | - | Same as above. |
| /ʃəl/ | `-RBL` | Yes | |
| /ʃəs/ | `-RBS` | Yes | |

For the finals above that have been labelled "Yes" under the Syllable Replacement column, that means that in cases where we need to represent the syllable as a whole chord in a write-out outline, we can use the final along with the joiner `SWR` to replace the conventional syllable stroke. For instance:

- digestion: `TKAOEUPBLG/SWR*ES/SWR-GS` (also `.../SH*OPB`)
- wonderful: `WOPBD/SWRER/SWR-FL` (also `.../STPUL`)

## Syllable Splitting

Syllable splitting refers to how multi-syllable words are split into sequences of strokes. By providing a single standard for splitting syllables, we can make outlines more predictable whilst reducing the dictionary size needed.

### Right Greedy Splitting

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Cocoa Theory chooses to use **right greedy splitting**, where each stroke tries to "consume" as many consonants to its right as "greedily" as possible. This comes with a few constraints:

- Final sounds cannot overlap
- Final sounds cannot break steno order; as mentioned before, asterisks are not considered when we talk about steno order.

Any consonants that fail to be grouped to the nearest vowels on their left will instead be grouped to the right; in cases where it cannot be grouped to the right, these consonants will constitute their own separate stroke, with the sounds being placed on the right.

If a non-starting syllable has no initials, we use the left joiner chord `SWR` to indicate that it should attach to the previous output. However, if a syllable does have initials, then we have to modify the left bank chord like so:

- **If the left bank chord is `KWR`, we do not modify it.** 
- **If the left bank chord does not contain `S-`, we add `S-`.** For example, the "rum" in "fulcrum" is `SRUM`, with the `S-` added to indicate that it should attach to the left; the full outline would thus be `TP*ULG/SRUM`.
- **If the left bank chord already contains `S-`, we add `*`.** For example, the "ship" in "hardship" is `SH*EUP`, with the asterisk added to indicate that it should attach to the left; the full outline would thus be `HARD/SH*EUP`. Note that this does not apply to just "s", but any left bank chord that contains `S-`. If the chord already contains an asterisk due to the right side, we can keep using the same asterisked stroke.

Right greedy splitting may seem unnatural to some on their first impression. With sufficient practice, however, it should become second nature. The advantage of right greedy splitting is that many of the split syllables tend not to be individual words themselves, allowing us to greatly reduce the number of boundary issues present in the theory.

### Dividing Clusters

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

There are clusters or partial clusters that some users may find difficult to divide purely greedily; there is thus some leniency in the way they are divided:

| Cluster | Greedy | Alternatives |
|---:|:---|:---|
| /stɹ/ | `...*S/SR...` | `...S/STR...` |
| /kstɹ/ (Spelled with x) | `...GT/SR...` | `...*BGS/STR...` |
| /tɹ/ | `...T/SR...` | `.../STR...` |
| /dɹ/ | `...D/SR...` | `.../STKR...` |
| "wr" | `...FB/SR...` | `.../SWR...` |

### Left Bank Glides

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

When the syllable starts with /j/ or /i/, we can use the `KWR` chord to indicate it; similarly, when a syllable starts with /w/, /u/, or /ʊ/, we can use the `W` key. However, there are cases where a user might try to insert these initials even though they have already been represented by the previous stroke. Whilst they are free to add such outlines, they are not part of the main theory:

- altruistic: `ALT/SRAOU/SWR*EUS/SWREUBG` (alt-ruu-ist-ic, not alt-ruu-wist-ic)
- piano: `PEU/SWRAPB/SWROE` (pi-an-oe, not pi-yan-noe)

### Syllable/Stroke Dropping

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Users who wish to take advantage of syllable or stroke dropping may do so, even though they are often based on stress patterns and thus are optional. It is important to still keep using the additional `S-` where applicable to indicate attached strokes to avoid boundary errors.

For words that have 2-stroke write-outs, no strokes can be dropped. 

For words that have 3-stroke write-outs, we can drop the centre stroke after giving any of its finals to the initial of the third stroke, if there is space. Note that 3-stroke write-outs do not necessarily correspond to 3-syllable words. Some examples include:

- similar: `SEUPL/SWREUL/SWRAR` → `SEUPL/SHRAR`
- preposition: `PREP/SWROS/SWREUGS` → `PREP/S*EUGS`
- filament: `TPEUL/SWRAPL/SWREPBT` → `TPEUL/SWR-PLT`

For words that have write-outs with more strokes, syllable dropping is based on stress. Some of these entries will be included in the dictionary, but there are currently no plans to include these write-outs for rarer words.

- similarly: `SEUPL/SWREUL/SWRARL/KWREU` → `SEUPL/SHRARL/KWREU`
- prepositional: `PREP/SWROS/SWREUGS/SWRAL` → `PREP/S*EUGS/SWRAL`
- hyperbolical: `HAOEUP/SWR*ERB/SWROL/SWREUBG/SWRAL` → `HAOEUP/SPWOL/SKAL`

### Consonant Greedy

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Consonant greedy is an alternative to syllable dropping that reduces the number of strokes per word, without relying on stress. This is accomplished by attempting to squeeze as many consonants or consonant clusters into each stroke as possible, ignoring the vowels between strokes or between consonants on the same side of a stroke, and ignoring any final consonants if the stroke can't accomodate more and the following stroke cannot include it in its initial. For instance:

- similarly: `SEUPL/SWREUL/SWRARL/KWREU` → `SPHEUL/SHREU` (smil-ly)
- prepositional: `PREP/SWROS/SWREUGS/SWRAL` → `PREPS/SHO*PBL`
- hyperbolical: `HAOEUP/SWR*ERB/SWROL/SWREUBG/SWRAL` → `HAOEUP/SPW*ERBLG/SWRAL`

In some cases, after putting as many consonants on the left, we are left with no vowels for the thumbs because the splitting point is immediately followed by another consonant. When this occurs, we simply shift the minimal amount of consonants from the left to the right so that we can have a vowel on the thumbs. If the vowel is represented by a no-key chord, that's still okay. For instance:

- cartography: `KR...` doesn't work, so `KART/STKPWRAF/KWREU`

To reduce the number of strokes needed for each word even further, we can make use of the inversions and folds introduced in the previous sections, as well as the `-FR` as M technique. For example:

- similarly: `SPHREURL`
- intricately: `SPWREUBLGT`

### -y Suffix

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

The "-y" suffix is written using `KWREU` and needs to be memorized explicitly. It also applies to cases where "y" is immediately followed by a final. Here are a few examples of it being used:

- happy: `HAP/KWREU`
- happily: `HAP/SWREUL/KWREU`
- methyl: `PH*ET/KWREUL`

This only applies when there are no initials, and the only vowel is "y" itself. If there are initials, the suffix would be written with the -y represented phonetically as `EU`.

Whilst this usually occurs at the end of words, it can also occur in the middle of words, which the user may not be used to due to its relative rarity. As such, these words are usually supplemented with outlines where `SWREU` is used instead. For example:

- anonymous: `APB/SWROPB/SWREUPL/SWROUS` or `APB/SWROPB/KWREUPL/SWROUS`
- analytics: `APB/SWRAL/SWREUT/SWREUBGS` or `APB/SWRAL/KWREUT/SWREUBGS`

## Edge Cases

### Silent Finals in French Loanwords

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

French loanwords often come with silent letters at the end; they can either be ignored in phonetic outlines, or included as part of orthographic outlines.

| Ending | Pronunciation | Full Orthographic | Standard |
|---:|:---|:---|:---|
| ailles | /aɪ/ | `AEUS` | `AEU` |
| ais | /eɪ/ | `AEUS` | `AEU` |
| ait | /eɪ/ | `AEUT` | `AEU` |
| eaux | /oʊ/ | `A*UBGS` | `AU` |
| er | /eɪ/ | `ER` | `AEU` |
| et | /eɪ/ | `ET` | `AEU` |
| ez | /eɪ/ | `EZ` | `AEU` |
| ieux | /juː/ | `AO*UBGS` | `AOU` |
| ioux | /juː/ | `O*UBGS` | `OU` |
| is | /i/ | `EUS` | `EU` |
| ois | /wɑ/ | `OEUS` | `WA` or `...AOU/SWA` |
| oix | /wɑ/ | `O*EUBGS` | `WA` or `...AOU/SWA` |
| ot | /oʊ/ | `OT` | `OE` |
| oup | /uː/ | `OUP` | `OU` |
| ous | /uː/ | `OUS` | `OU` |
| oux | /uː/ | `O*UBGS` | `OU` |

This is by no means an exhaustive list, but outlines for such words generally follow either their spelling or purely phonetically. Alternatively, we can also write the vowel orthographically, but drop the silent letter at the end.

### Greek and Latin Plurals

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

The regular `-S` stroke will not work properly on words with irregular Greek or Latin plurals. Instead, they are stroked as if the plural form is a separate word. This is such that in cases where both the irregular and regular plurals are accepted, they can both be stroked in a predictable manner. 

| Singular | Plural | Origin | Examples |
|---:|:---|:---|:---|
| a | ae | Latin 1st Declension | larva `HRAFRB/SWRA`, larvae `HRAFRB/SWRAE` |
| us | i | Latin 2nd Declension Masc. | radius `RAEUD/KWRUS`, radii `RAEUD/SWREU/SWRAOEU` or `RAEUD/KWRAOEU` |
| um | a | Latin 2nd Declension Neut. | minimum `PHEUPB/SWREUPL/SWRUPL`, minima `PHEUPB/SWREUPL/SWRA` |
| ex | ices | Latin 3rd Declension | vertex `SRERT/SWR*EBGS`, vertices `SRERT/SWREUS/SWRAOES` |
| ix | ices | Latin 3rd Declension | matrix `SRERT/SWR*EBGS`, matrices `SRERT/SWREUS/SWRAOES` |
| is | es | Latin 3rd Declension | axis `A*BGS/SWREUS`, axes `A*BGS/SWRAOES` |
| ur | ora | Latin 3rd Declension | femur `TPAOEPL/SWRUR`, femora `TPAOEPL/SWROR/SWRA` |
| us | ora | Latin 3rd Declension | corpus `KORP/SWRUS`, corpora `KORP/SWROR/SWRA` |
| us | era | Latin 3rd Declension | genus `SKWRAOEPB/SWRUS`, genera `SKWRAOEPB/SWRER/SWRA` |
| on | a | Greek 2nd Declension Neut. | criterion `KRAOEUT/SWRAOER/KWROPB`, criteria `KRAOEUT/SWRAOER/KWRA` |
| a | ata | Greek 3rd Declension Neut. | stoma `STOEPL/SWRA`, stomata `STOEPL/SWRAT/SWRA` |
| us | odes | Greek 3rd Declension Masc./Fem. | octopus `OBGT/SWROP/SWRUS`, octopodes `OBGT/SWROP/SWROEDZ` (TBC: Subject to change due to vowels) |

## Common briefs

![](https://img.shields.io/badge/-to%20be%20expanded-blue?style=for-the-badge&logo=)

Briefs refer to outlines that do not strictly follow all the core rules listed before. Groups of briefs may still have internally consistent patterns, but they would still have to be explicitly memorized. 

Here is a list of briefs for the most common words. Mandatories are generally avoided, but for the most common words, their briefs are still recommended over their rule-based outlines such that phrasing is made simpler.

| Word | Chord | Mandatory | Remarks |
|---:|:---|:---|:---|
| the | `-T` | Yes | `THE` is assigned to "they" |
| be | `-B` | Yes | `PWE` is currently reserved for the "be-" prefix. |
| of | `-F` | Yes | `OF` is assigned to "off" |
| and | `SKP` | | `APBD` also works, but the brief is always recommended. |
| a | `A` | | `AEU` also works. |
| is | `S` | Yes | |
| are | `R` or `-R` | Yes | |
| was | `-FS` | | `WAS` also works and is taught first. `-FS` is mostly used in phrasing. |
| were | `WR` or `-RP` | Yes | `-RP` is mostly used in phrasing. |
| in | `TPH` | Yes | |
| this | `TH` | | `THEUS` also works, but the brief is recommended. |
| that | `THA` | Yes | `THAT` is assigned to "that the". |
| those | `THOS` | | `THOZ` and `THOEZ` also work. |
| these | `THES` | | `THEZ` and `THAOEZ` also work. |
| have | `SR` | | `HA*F` also work. |
| I | `EU` | Yes | |
| you | `U` | Yes | |
| it | `T-` | | |
| it's | `T-S` | | "its" is `EUTS`, "it is" is `T*S`. |
| they | `THE` | | `THEFB` also works, but the brief is recommended. |
| for | `TP-R` | Yes | `TPOR` is assigned to "fore" |
| with | `W` | | `W*EUT` also works, but the brief is recommended. |
| without | `WOUT` | | `W*EUT/SWROUT` also works. |
| did | `TK` | | |
| doing | `TKAOG` | | `TKOG` is assigned to "dog". |
| but | `TPW` | | `PWUT` also works. "butt" is `PW*UT` or `PWUT/SWR-T`. |
| by | `PW` | Yes | `PWAOEU` is "bi" and `PWAOEUFB` is "buy". |
| from | `TPR` | | `TPROPL` also works, but the brief is recommended. |
| will | `HR` | | `WEUL` also works, but the brief is recommended. |
| would | `WO` | | `WOULD` also works, but the brief is recommended. |
| can | `K` | | `KAPB` also works, but is more commonly used in contexts such as "metal can". |
| could | `KO` | | `KOULD` also works, but the brief is recommended. |
| should | `SHO` | | `SHOULD` also works, but the brief is recommended. |
| my | `PHEU` | | `PHAOEUFB` also works, but the brief is recommended. |
| one | `WUPB` | | A weird quirk of the English language. Should be memorized along with "once" `WUPBS`. |
| there | `TH-R` | Yes | See "their" and "they're" below. |
| their | `THAEUR` or `THAER` | | See surrounding entries for "there" and "they're". |
| they're | `THER` | Yes | See "there" and "their" above. |
| what | `WHA` | Yes | `WHAT` is assigned to "what the". |
| which | `WEU` | | `WHEUFP` is the rule-based outline; `WEUFP` is "witch". |
| when | `WH` | | `WHEPB` also works, but the brief is recommended. |
| whether | `WHR` | | `WH*ET/SWRER` also works. |
| why | `KWR` | | `WHAOEUFB` also works, but the brief is recommended. |
| if | `TP` | Yes | |
| just | `SKWR` | | `SKWR*US` also works, but the brief is recommended. |
| into | `TPHAO` | | Inherited from Plover. |
| go | `TKPW` | | `TKPWO` also works. |
| good | `TKPW-D` | | `TKPWAOD` also works. |
| some | `SPH` | | `SOPL` also works. |
| other | `OER` | | "o'er" is `O*ER` and is a mandatory. |
| only | `OPBL` | | |
| over | `OEFR` | | |
| because | `PWAU` | | While some other theories use `PWAUS`, the `-S` has been removed here such that phrase briefs such as `PWAUF` for "because of" would fit steno order. |
| away | `WAU` | | Completely arbitrary. `AFB/SWRAEUFB` also works. |
| about | `P` | | |

"n't" is attached with `-PBT`, and "'ve" is attached with `*F`. For instance:

- didn't: `TK-PBT`
- would've: `WO*F`

## Numbers

### Single Digits & Trailing Zeros

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

Cocoa Theory uses the right hand numpad system for numbers. Digits are entered like so:

| Digit | Chord | Digit | Chord | Digit | Chord |
|---:|:---|---:|:---|---:|:---|
| 7 | `#-F` | 8 | `#-P` | 9 | `#-L` |
| 4 | `#-FR` | 5 | `#-PB` | 6 | `#-LG` |
| 1 | `#-R` | 2 | `#-B` | 3 | `#-G` |
| 0 | `#E` | 00 | `#U` | 000 | `#EU` |

While numbers are usually entered digit-by-digit, we can add one to three zeros by using the `EU` keys:

- 40: `#EFR`
- 200: `#UB`
- 8000: `#EUP`

### Two-digit and Three-digit Numbers

![](https://img.shields.io/badge/-stable-green?style=for-the-badge&logo=)

We can write 2 to 3 digit numbers that don't end with 0 if they are on different columns and follow steno order from left to right. For example:

- 23: `#-BG`
- 489: `#-FRPL`
- 12600: `#URBLG`

We can also add an additional digit 5 by including the `-S` key, like so:

- 65: `#-LGS`
- 835: `#-PGS`
- 1550: `#ERPBS`

These additions will always come before the zeroes represented by the thumb keys.

### Number modifiers

![](https://img.shields.io/badge/-to%20be%20expanded-blue?style=for-the-badge&logo=)

There are also these additional modifiers, which change how the output is formatted:

| Modifier | Key/Chord | Example | On its own |
|---:|:---|:---|:---|
| Ordinal | `-T` | 3rd: `#-GT`, 25th: `#-BTS` | . (Point separator) |
| Plural | `-Z` | 80s: `#EPZ`, 90s: `#ELZ` | , (Comma separator) |

These modifiers are not stackable.

## Symbols

Cocoa Theory has its own system for symbols, but it was also made to be compatible with Emily's Symbols should the user choose to use that.

### Punctuation

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

Most punctuation is done with `KW` on the right and either a phonetic or shape-based memorization hook on the thumb keys and right bank keys.

| Punctuation | Description | Chord |
|---:|:---|:---|
| .␣ | Full Stop / Period | `-FPLT` or `TP-PL` |
| . | Decimal Point | `#-T` or `P-P` |
| ,␣ | Comma | `-RBGS` or `KW-BG` |
| , | Decimal Comma | `#-S` or `W-B` |
| ?␣ | Question Mark | `KW-FPG` or `KW-PL` |
| !␣ | Exclamation Mark | `KW-PB` or `TP-BG` |
| :␣ | Colon | `KWUF` |
| ;␣ | Semicolon | `KWEUF` |
| ' | Apostrophe | `KW-F` |
| ␣\` | Backtick | `KW-PG` |
| ␣' | Opening Single Quote | `KW-P` |
| '␣ | Closing Single Quote | `KW-L` |
| ␣" | Opening Double Quote | `KW-FP` |
| "␣ | Closing Double Quote | `KW-LT` |
| ␣\` | Opening Backtick | `KW-FB` |
| \`␣ | Closing Backtick | `KW-LS` |
| ␣( | Opening Parenthesis | `KWURP` |
| )␣ | Closing Parenthesis | `KWUPG` |
| ␣[ | Opening Bracket | `KWUFP` |
| ]␣ | Closing Bracket | `KWUPG` |
| ␣{ | Opening Brace | `KWURPB` |
| }␣ | Closing Brace | `KWUPBG` |
| / | Forward Slash | `KW-RL` |
| \\ | Backslash | `KW-FG` |
| * | Asterisk | `KW-PBLG` |
| @ | At | `KWAT` |
| ␣-␣ | Hyphen | `KW-RBG` |
| - | Joining Hyphen | `KW-FPL` |
| ~␣ | Tilde | `KW-RPL` |
| ^ | Caret | `KW-RPG` |
| ...␣ | Ellipsis | `KW-BS` |
| ␣&␣ | Ampersand | `KW-FRPBG` or `SKP*` |

### Diacritics

![](https://img.shields.io/badge/-to%20be%20documented-yellow?style=for-the-badge&logo=)

Diacritics are not the priority right now and will be handled in the future using a plugin. 

## Formatting

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

Formatting control is done using a collection of "half-strokes". These are a work-in-progress.

| Description | Chord |
|---:|:---|
| Cycle Alternatives | `-RB` |
| Insert Space | `SP` |
| Suppress Space | `SWR` |
| Retro Insert Space | `SP-D` |
| Retro Suppress Space | `SWR*` |
| All Uppercase Next | `-PBLG` |
| Capitalize Next | `-PL` |
| Lowercase Next | `-BG` |
| Proper Noun Next | `-FP` |
| Retro Capitalize | `-PLD` |
| Retro Lowercase | `-BGD` |
| Retro Proper Noun | `-FPD` |
| Orthographic | `-PL` |
| Orthographic Capitalize | `-FPL` |
| Retro Orthographic | `-PLD` |
| Steno Correction | `*` |
| Delete Word | `SW` |
| Return and Capitalize | `R-R` |
| Return and Keep Case | `R-RB` |

## Modifiers

![](https://img.shields.io/badge/-to%20be%20documented-yellow?style=for-the-badge&logo=)

Cocoa is designed to be compatible with Emily's Modifiers, but they would have to be adapted slightly to the new fingerspelling alphabet.

## Orthographic System

The orthographic system is a system within Cocoa Theory intended to be an intermediate fallback for words that aren't in the dictionary, such that users can write unknown or foreign words quickly without resorting to fingerspelling. It is entirely orthographic, where chords are determined entirely based on spelling. For example:

> "Tagalog ay isa sa mga pinakaginagamit na wika ng Pilipinas"<br>
> `-FPL/TAG/KWHAL/KWHOG . -PL/ABZ . EUS/KWHA . -PL/SA . PH-G/KWHA . PEUPB/KWHALG/KWHAG/KWHEUPB/KWHAG/KWHAPL/KWHEUT . -PL/TPHA . WEULG/KWHA . -PL/-PBG . -FPL/PEUL/KWHEUP/KWHEUPB/KWHAS`

Many of the chords in the orthographic system differ from the main theory, since we have to create different chords for groups of letters that would otherwise be pronounced the same way (thus require no distinction phonetically).

Due to the large output space of the orthographic system, it can only be realistically implemented as a programmatic dictionary; it is thus only available on Plover. Orthographic words must either have the `KWH` chord, or alternatively use one of the orthographic formatting chords - `-PL`, `-FPL`, or `-PLD`.

Since the system also uses the number key, it is expected to conflict with both numbers and the phrasing system. In these cases, it is better to use the orthographic system formatting strokes to avoid boundary issues with numbers and phrases. 

### Initials

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

Initials mostly resemble their phonetic counterparts. The largest exception is the linker, which is replaced with `KWH` - it is used to link the current stroke to the previous output, when there is no initial. When there is an initial, we add the number key `#` instead. Note that whenever a word is stroked using the orthographic system without ever using the `KWH` linker, we must use an orthographic formatting stroke at the front (`-PL` or `-FPL`) or back (`-PLD`) to indicate it.

| Initial | Chord | Derivatives | Remarks |
|---:|:---|:---|:---|
| (Linker) | `KWH` | | We can use `#KWH` to double the previous letter. |
| b | `PW` | br `PWR`, bl `PWHR`, bh `PWH` | |
| c | `KPW` | ch `KPWH`, cr `KPWR`, cl `KPWHR` | |
| chl | `KWHR` | | Conflicts with the much rarer initial "ql" |
| chr | `KHR` | | Conflicts with the much rarer initial "kl" |
| cz | `SKP` | | |
| d | `TK` | dr `TKR`, dh `TKH`, dw `TKW` | |
| f | `TP` | fr `TPR` | |
| fl | `TPHR` | | Explicit entry added to avoid confusion with "nr". |
| ph | `TKP` | phr `TKPR` | |
| phl | `TKPHR` | | Explicit entry added to avoid confusion with "knr" |
| g | `TKPW` | gr `TKPWR`, gl `TKPWHR`, gh `TKPWH` | |
| gn | `STKPW` | | |
| h | `H` | | |
| j | `SKWR` | | |
| k | `K` | kr `KR`, kh `KH` | |
| kl | `KP` | | |
| l | `HR` | | |
| (Double) + l | `SKPHR` | | Doubles previous letter and adds "l" | 
| m | `PH` | | |
| n | `TPH` | | |
| kn | `TKPH` | | |
| p | `P` | pr `PR` | |
| pl | `PHR` | | Explicit entry added to avoid confusion with "mr". |
| pn | `TPW` | | |
| ps | `STP` | | |
| pt | `TWR` | | |
| q | `KW` | | |
| r | `R` | | |
| (Double) + r | | Doubles previous letter and adds "r" |
| rh | `KPR` | | |
| s | `S` | st `ST`, sp `SP`, sh `SH`, sc `SKPW`, str `STR`, sl `SHR`, sw `SW`, sn `STPH`, sk `SK`, scr `SKPWR`, sm `SPH`, sch `SKPWH`, spl `SPHR`, spr `SPR`, scl `SKPWHR`, skr `SKR` | |
| shr | `SKHR` | | Conflicts with sl, which has been assigned to `SHR`. |
| sq | `STK` | | Conflicts with z, which has been assigned to `SKW`. |
| sph | `STKP` | | Explicit entry so that it won't be misinterpreted as "sqh". |
| t | `T` | tr `TR`, th `TH`, tw `TW` | |
| thr | `THR` | | Conflicts with tl |
| thw | `TWH` | | |
| ts | `STW` | | |
| tz | `STKW` | | |
| v | `SR` | | |
| w | `W` | wh `WH`, wr `WR` | |
| x | `SKPH` | | |
| y | `KWR` | | |
| z | `SKW` | | |
| zh | `STWH` | | Although `SKWH` works, we provide an alternative to prevent conflicts with Emily's Symbols |

Not all initials are covered by the list below, mostly because they are too rare to justify having their own chord. In those cases, we can simply use the final to write the initial in a single stroke:

- mn: `PH-PB`
- ng: `TPH-G`
- scht: `SKPWH-T`

### Medials

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

To access the variant, add the asterisk `*` to the chord.

| Chord | Medial | Variant | Remarks |
|---:|:---:|:---:|:---|
| (Empty) | (Empty) | y | |
| `A` | a | ua | |
| `O` | o | eo | |
| `AO` | oo | ao | |
| `E` | e | eou | |
| `AE` | ea | ae | |
| `OE` | oa | oe | |
| `AOE` | ee | ui | |
| `U` | u | uo | |
| `AU` | au | ye | |
| `OU` | ou | iou | |
| `AOU` | ue | eu | |
| `EU` | i | iu | |
| `AEU` | ai | ei | |
| `OEU` | oi | io | |
| `AOEU` | ia | ie | |

Here are some examples of the medials in use:

- cautious: `KPWAUT/KWHO*US`
- keine: `KA*EUPB/KWHE`

### Finals

![](https://img.shields.io/badge/-unstable-red?style=for-the-badge&logo=)

Finals are more expressive than initials due to right hand syllable splitting, due to the right bank containing more than one key. 

Note that whenever we encounter a doubled consonant letter, we can use the doubling initial joiner for it. This eliminates the need to create dedicated final strokes for doubled letters such as "tt" or "dd", but some of them are still included due to their high frequency.

In many of these chords, we add either a `-Z`, `-D`, or `-F` to avoid conflicts.

| Final | Chord | Derivatives | Remarks |
|---:|:---|:---|:---|
| b | `-B` | bs `-BS`, bt `-BT`, bl `-BL` | |
| c | `-BG` | ct `-BGT`, cts `-BGTS` | `-BG` is used for "c" as it is more common; k has been assigned another chord |
| ch | `-FP` | chs `-FPS`, cht `-FPT`, chts `-FPTS` | |
| ck | `-BLG` | cks `-BLGS` | |
| d | `-D` | | |
| ddl | `-FLGDZ` | | Extended from "dl" by adding `-F` |
| dg | `-GD` | | |
| dl | `-LGDZ` | | From Ireland's Stenotypy |
| f | `-F` | ft `-FT`, fs `-FS`, fts `-FTS` | |
| g | `-G` | | |
| gh | `-PG` | ght `-PGT`, ghts `-PGTS`, ghs `-PGS` | |
| gm | `-PLG` | | |
| gn | `-PBGZ` | | `-Z` used to indicate inversion |
| gs | `-GSZ` | | `-Z` used to avoid conflict with "tion" |
| h | `-PZ` | | |
| j | `-PBLG` | | |
| k | `-LG` | | Arbitrary chord assigned to separate it from "c" |
| kh | `-PLGZ` | | Stacked "k" and "h" |
| ks | `-LGS` | | |
| l | `-L` | ls `-LS`, ld `-LD`, lt `-LT`, lts `-LTS` | |
| lb | `-BLZ` | | `-Z` used to indicate inversion and avoid conflict with "bl" |
| lc | `-BLGZ` | | Stacked "l" and "c", `-Z` used to avoid conflict with "ck" |
| lch | `-LGZ` | | `-Z` used to avoid conflict with "k" |
| lf | `-FLZ` | | `-Z` used to indicate inversion |
| lg | `-LGD` | | `-D` used since `-LGZ` taken by "lch" |
| lk | `-FRLG` | | Arbitrary chord assigned to avoid conflicts |
| ll | `-LZ` | | |
| lm | `-FRLZ` | | `-FR` used for "m", `-Z` used to indicate inversion |
| ln | `-PBLZ` | | `-Z` used to indicate inversion |
| lp | `-PLD` | | `-Z` used to indicate inversion |
| lph | `-FLD` | | |
| lth | `-LTD` | | |
| m | `-PL` | | |
| mb | `-FRB` | mbs `-FRBS` | `-FR` used for "m" |
| ment | `-PLT` | | |
| ml | `-FRL` | | `-FR` used for "m" |
| mn | `-FRPBD` | | `-D` used to avoid conflict with "nch" |
| mp | `-FRP` | mps `-FRPS`, mpt `-FRPT`, mpts `-FRPTS` | |
| mph | `-FPLZ` | | `-Z` used to avoid conflict with "sm" |
| n | `-PB` | ns `-PBS`, nd `-PBD`, nst `-PBSZ`, nt `-PBT`, nth `-PBTH`, nts `-PBTS` | |
| nc | `-FRPBGZ` | | `-Z` used to avoid conflict with "nk" |
| nch | `-FRPB` | nchs `-FRPBS` | |
| nct | `-FRPBGT` | | Note that this chord isn't used for "nkt" |
| ng | `-PBG` | ngth `-PBGTD` | |
| ngs | `-PBGS` | | |
| nk | `-FRPBG` | nks `-FRPBGS` | See "nc" |
| nm | `-FRPBDZ` | | `-DZ` used to avoid conflict with "nch" |
| nx | `-FRPBGSZ` | | |
| p | `-P` | ps `-PS`, pt `-PT`, pts `-PTS` | |
| ph | `-FZ` | | `-Z` used to avoid conflict with "f" |
| pl | `-PLD` | | `-D` used to avoid conflict with "m" |
| q | `-GZ` | | Arbitrary chord assigned to separate it from "c" and "k" |
| r | `-R` | rs `-RS`, rd `-RD`, rm `-RPL`, rt `-RT`, rk `-RLG`, rn `-RPB`, rts `-RTS`, rks `-RLGS`, rms `-RPLS`, rns `-RPBS`, rl `-RL`, rth `-RTD`, rp `-RP`, rls `-RLS`, rg `-RG`, rst `-RSZ`, rps `-RPS`, rgs `-RGSZ`, rld `-RLD`, rnt `-RPBT`, rgh `-RPG` | |
| rb | `-RBZ` | | `-Z` used to avoid conflict with "sh" |
| rc | `-RBG` | | |
| rch | `-FRPBZ` | | `-Z` used to avoid conflict with "nch" |
| rf | `-FR` or `-FRZ` | rfs `-FRS` | `-Z` can be used to indicate inversion, but is not necessary. |
| rph | `-FRD` | | `-D` used to avoid conflict with "rf" |
| rv | `-FRBD` | | `-D` used to avoid conflict with "mb" |
| rw | `-FRBZ` | | `-Z` used to avoid conflict with "mb" |
| s | `-S` | | |
| sc | `-FBG` | | |
| sch | `-FPSZ` | | `-Z` used to indicate inversion |
| sh | `-RB` | sht `-RBT` | |
| sk | `-FLG` | | |
| sm | `-FPL` | sms `-FPLS` | |
| sp | `-FPZ` | | `-Z` used to avoid conflict with "ch" |
| ss | `-TSDZ` | | |
| st | `-SZ` | | `-Z` used to avoid conflict with "s" |
| t | `-T` | ts `-TS` | |
| tch | `-FPTD` | | `-D` used to indicate inversion |
| th | `-TD` | | `-D` used to avoid conflict with "t" |
| tion | `-GS` | | |
| tl | `-LGTS` | | From Ireland's Stenotypy |
| ttl | `-FLGTS` | | Extended from "tl" by adding `-F` |
| v | `-FD` | | `-D` used to avoid conflict with "f" |
| w | `-FB` | ws `-FBS`, wl `-FBL`, wls `-FBLS`, wk `-FBLG`, wth `-FBTD`, wd `-FBD`, wks `-FBLGS`, wt `-FBT` | |
| x | `-BGS` | | Since the asterisk is for medials, we don't use the asterisk here |
| xt | `-GT` | xts `-GTS` | |
| y | `-BZ` | | Arbitrary chord assigned to separate it from "w" |
| z | `-Z` | | |


## Phrasing System

![](https://img.shields.io/badge/-work%20in%20progress-orange?style=for-the-badge&logo=)
