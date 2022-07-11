# Cocoa Theory Specifications

This is a documentation for Cocoa Theory, a stenographic theory for writing English on the Ward Stone Ireland layout. 

It should not be used as a primary learning resource and was written to provide a brief overview of the core rules and design decisions in the theory. Things will seem a lot more complicated than they actually are in this document, but only because it is trying to be as dense and complete as possible.

## Design Objectives

Cocoa Theory is derived from Plover Theory, with heavy influences from Phoenix and Realwrite/Realtime, as well as theory ideas floating around on the Plover Discord. It is a mixed (phonetic-orthographic) theory with heavy use of orthographic disambiguation. It was initially created as a variant of Plover Theory to fix three major problems with the theory: Reliance on stress-based syllable dropping, lack of consistency in syllable splitting, and the overuse of disambiguation by asterisks. Since then, it has undergone enough changes to be considered an independent theory. The main design goals are:

- To remove dependence on stress-based syllable dropping, as not all English speakers are capable of identifying stressed and unstressed syllables. This does not indicate the complete removal of stress-based syllable dropping, but merely makes it optional;
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

### Overloaded Initials

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
| kn | TBC | |
| ph | TBC | |

In cases where disambiguation is not necessary, such as "knife", both the phonetic (`TPHAOEUF`) and the orthographic stroke (`knAOEUF`) should be provided, chosen by the user based on preference. 

There are also many cases where we include the orthographic entry not for disambiguation, but to anticipate situations where the speaker actually pronounces these words based on how they are spelled, unaware of the exceptions in English orthography. 

Note that initial gh- is written as `TKPW`, not `TKPWH`. The latter chord may be used for disambiguation if necessary, but I have not come across any situations where I have required it so far. Hence the following words are written with `TKPW`:

- gherkin: `TKPWERBG/SWREUPB`, not `TKPWHERBG/SWREUPB`
- ghetto: `TKPWET/SWROE`, not `TKPWHET/SWROE`

Nevertheless, there isn't actually anything bad with the chord `TKPWH`, so the user can add it for words starting with gh- if they so choose to.

### Advanced Initials

These initials are either memorized or constructed from the principles listed previously, but they are mostly used in briefs rather than syllable-based outlines.

| Initial | Pronunciations | Chord | Remarks |
|---:|:---|:---|:---|
| des, dis | /dɪs/ | `STK` | |
| exp, and, end | /ɪksp/, /ænd/, /ɛnd/ | `SKP` | |
| imp, emp | /ɪmp/, /ɛmp/ | `STKPW` | TBC |
| int, ent | /ɪnt/, /ənt/, /ɛnt/, /ɑnt/ | `SPW` | |
| ext | /ɪkst/, /ɛkst/ | `SKPW` | |
| inf | /ɪnf/ | `STKPH` | |
| adv | /ædv/, /ədv/ | `STKW` | |
| inv | /ɪnv/ | `STPHR` | |
| ins, ens, inst | /ɪns/, /ɛns/, /ɑns/, /ɪnst/ | `STPH` | |
| rev, riv, rew, rw | /ɹəv/, /ɹɪv/, /ɹəw/, /ɹɪw/ | `WR` | |

### Initial Joiners

There are also two joiners, used to indicate the lack of an initial consonant sound. These are explained in the syllable splitting section.

- Generic initial joiner: `SWH`
- Orthographic joiner: `KWH`

Since `KWH` is reserved as the orthographic joiner, we cannot use it for the chw- sound, present in words such as "factual" or "eventually". As mentioned previously, that sound uses the `TW` chord instead - if necessary, this can be seen as an orthographic chord. 

### T and D

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

If any vowel clusters are spelled with the following sequences of letters, then they are stroked orthographically regardless of pronunciation:

| Spelling | Chord |
|---:|:---|
| ai | `AEU` |
| au | `AU` |
| ae, ea | `AE` |
| ea | `AE` |
| oo, oa, ao | `AO` (TBC: Subject to change due to boot/boat, check oo/oa min. pairs) |
| aou, oau | `AOU` |
| ou | `OU` |

There are instances where we find these spellings in vowel clusters that would be considered as two syllables, such as the "oo" in coordination. In these cases, we can apply the orthographic overrides as usual, or split it into two syllables. Some examples include:

- "oo" in "coordination": `KAORD/SWREUPB/SWRAEUGS` or `KOE/SWRORD/SWREUPB/SWRAEUGS` or `KO/SWRORD/SWREUPB/SWRAEUGS`
- "ea" in "reality": `RAEL/SWREUT/KWREU` or `RAOE/SWRAL/SWREUT/KWREU` or `RE/SWRAL/SWREUT/KWREU`

There are also instances where we find these spellings as part of a longer string of vowels. We will still write them with the orthographic override. If a string contains multiple orthographic overrides, follow the rightmost one. Since these words tend to be rarer and are typically loanwords, we can afford to be more lenient with them.

### W and Y as Vowels

Some vowel sounds require us to write with spelling. In some cases, the letters "y" and "w" may be used to spell those vowels. In those cases, we use the chords `EU` and `AOU` to represent them respectively. For instance:

- "y" in myth: `PH*EUT`
- "w" in crwth: `KRAO*UT`

### Short Vowels

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
| comma (schwa) | around `AR/SWROUPBD`, vodka `SROD/SKA` | |

We will often find words that cannot be stroked by spelling, because the combination of letters used to represent the vowel is too rare to warrant a special chord. In this case, we stroke them phonetically, using the fallback column. If the fallback column is empty, then we take the rightmost vowel. For example:

- "ie" in "friend": `TPREPBD`
- "ue" in "conquer": `KOFRPBG/SWRER`

When the spelling of a word deviates too much from its spelling, we will also offer a phonetic outline, using the fallback chord associated with the vowel. For instance:

- "u" in "minute": `PHEUPB/SWREUT`
- "o" in "women": `WEUPL/SWREPB`

For the palm vowel specifically, whenever the vowel is spelled as "au", "al", or "aw", we use `AU` instead of `A`, as with the outline listed for "balm".

Note that the thought vowel has been excluded from the list of short vowel set; it has instead been included in the long vowel list.

### Long Vowels

Long vowels are all vowels that aren't short, including diphthongs. All of them have a base chord, but since conflict rates are often high, they all have a list of associated disambiguators, each corresponding to a possible spelling of the vowel.

~ is a consonant wildcard. Note that orthographic overrides take priority.

| Lexical Set | Base Chord | Disambiguators |
|---:|:---|:---|
| fleece | `AOE` | i `EU` |
| face | `AEU` | ei `AE`, ey `EFB`, ay `AEUFB`, a~e `AEF` |
| thought | `AU` | o `O`, aw `AUFB`, ou `OU` |
| goat | `OE` | o `O`, ow `OEFB` |
| goose | `AOU` | o `O`, u `AOU`, ew `AOUFB`, o~e `OE` |
| price | `AOEU` | y `AOEUFB`, uy `UFB`, ye `AOEUFB`|
| choice | `OEU` | oy `OEUFB` |
| mouth | `OU` | ow `OUFB` |

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

### Exceptions for a~e

The "a~e" pattern is stroked as `AEF`, like so:

- base: `PWAEFS`
- rate: `RAEFT`
- taste: `TA*EFS`
- fame: `TPAEFPL`

Note that clusters containing multiple consonants can also be matched with the "~" wildcard. 

This is mainly to avoid conflicts with the "ai" vowel spelling, which often is pronounced the same way. However, there is one single exception to this rule - when used with `-P`, this can conflict with any syllables ending with "-each", such as "teach" and "tape". Thus for /p/ specifically, we will stick to the base chord:

- tape: `TAEUP`

Additionally, the `AEF` pattern does not apply to other similar patterns with a silent "e":

- praise: `PRAEUS`, not `PRAEFS` or `PRAEUFS`
- prose: `PROES`, not `PROEFS`

### Vowels before R

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

### Disambiguators in Conjugated Words

When words are conjugated or modified with affixes, the vowel strings that determine which chord or disambiguator we use may change. In these instances, we can choose to use either the original chord, or to ignore it and construct the outline based on the new modified spelling:

- bellies: `PWEL/SWREU/-S` or `PWEL/KWREU/-S`
- casing: `KAEFS/-G` or `KAEUS/-G`

### Difficult vowels

When long vowels are written with a single letter, some users may find it difficult to use the actual long vowel chord rather than the single letter key/chord corresponding to the letter. Cocoa Theory tries to account for this specifically for the goat vowel by including both the orthographic and phonetic variants:

- "o" in "macho": `O` or `OE`

Another problem is when a word starts with an e-, which can either be pronounced as the fleece vowel, or as a reduced schwa. Again, both variants would be included:

- "e" in "ecology": `E` or `AOE`

### OEU Briefing

The `OEU` chord is also sometimes used for one of two things:

- To indicate that there is an additional -y after the current syllable, such as in "happy". Whilst Plover Theory also uses `AE` for this purpose, Cocoa only uses `OEU`, and applies it to a much smaller selection of words. (TBC: Experiment with `-DZ` for final -y, or some other pinky chord)

- As a wildcard, to provide an alternative to skeletal briefs.

These two uses should not be treated as consistent rules, but rather as briefing techniques.

## Finals

Whilst finals are mostly stroked phonetically, there are too many orthographic finals that it would be odd to call it phonetic. With that in mind, due to the syllable splitting used in the theory, finals play an extremely important role in representing complex consonant clusters, much more complex than on the left bank (appropriate given that the right bank has more keys).

Still, similar to initials, we can expect most silent letters to be ignored, unless any of the following sections say otherwise. Also similar to initials, if there is an orthographic disambiguator available for a given final, but no conflict is present, both the phonetic and orthographic outlines should be offered.

### Orthographic Overrides

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
| /ɹtʃ/ | `-FRPB` | TBC: Conflicts with -nsh |
| /ltʃ/ | `-LG` | |
| /nʃ/ | `-PBZ` | |
| /ɹʃ/ | `-RZ` | TBC: Conflicts with -rize |
| /lʃ/ | `-LZ` | TBC: Conflicts with -lize |
| /ɹb/ | `*RB` | Prevent conflicts with -sh |
| /ɹv/ | `-FRB` | |
| /lk/ | `*LG` | |
| /lp/ | `-P` | /l/ is ignored. |
| /lm/ | `-PL` | /l/ is ignored. In many cases, the "l" is accounted for as part of the vowel, such as "calm" `KAUPL` |

When arranging chords in steno order, we can safely ignore asterisks. For instance, /ɹst/ is `*RS`, since we can ignore the asterisk in `*S` and consider `*S` as a chord that comes after `-R`. 

### Final Inversion

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

As stated before, the letters "t" and "d" are often pronounced as /tʃ/ and /dʒ/. In these cases, they should be stroked orthographically, as it can be rather difficult to predict when such pronunciations occur. However, they can be stroked phonetically sometimes, based on the General American accent:

- nature: `NAEUT/SWRAOUR` or `NAEUT/SWRUR` or `NAEUFP/SWRAOUR` or `NAEUFP/SWRUR`
- graduate (verb): `TKPWRAD/SWAEFT` or `TKPWRAPBLG/SWAEFT`

Users are recommended to either use the orthographic outlines, or to define their own phonetic outlines to fill in the gaps of the dictionary based on their personal preferences.

### Folded Suffixes

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

Similar to how `-F` can represent "s", we can use `-FR` to represent the /m/ sound whenever we cannot represent a cluster that contains the sound properly using steno order without overlapping. For instance:

| Cluster | Chord | Remarks |
|---:|:---|:---|
| /mp/ | `-FRP` | |
| /mk/ | `-FRBG` | |
| /mn/ | `-FRPB` | |
| /ml/ | `-FRL` | |
| /mb/ | `-FRB` | There are instances where the "b" in "mb" is silent, but this can be difficult to predict. Hence `-FRB` is used to represent "mb" in all instances as an orthographic override, rather than a phonetic chord. |

### Asterisk Dropping in V and Z

For convenience, the asterisk in `*F` used to represent /v/ can be dropped whenever there are no conflicts. For instance:

- rave: `RAEF` or `RA*EF`
- save: `SA*EF`, but not `SAEF` due to conflict with "safe"

This can also apply to instances where `*F` is used to represent "z":

- freezer: `TPRAOEFR` or `TPRAO*EFR`
- razer: `RA*EUFR`, but not `RAEUFR` due to conflict with "racer"

### Advanced finals

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
| /ʃən/, /ʒən/, /dʒən/ | `-GS` | Yes | |
| /nʃən/, /neɪʃən/ | `-PBGS` | - | Also applies to any of the -shun variants above. |
| /kʃən/, /keɪʃən/ | `-BGS` | - | Same as above. |
| /lʃən/, /luːʃən/, /luːʒən/ | `-LGS` | - | Same as above. |
| /ŋkʃən/ | `-FRPBGS` | - | Same as above. |
| /ʃəl/ | `-RBL` | Yes | |
| /ʃəs/ | `-RBS` | Yes | |

For the finals above that have been labelled "Yes" under the Syllable Replacement, that means that in cases where we need to represent the syllable as a whole chord in a write-out outline, we can use the final along with the joiner `SWR` to replace the conventional syllable stroke. For instance:

- digestion: `TKAOEUPBLG/SWR*ES/SWR-GS` (also `.../SH*UPB`)
- wonderful: `WOPBD/SWRER/SWR-FL` (also `.../STPUL`)

### Silent Finals in French Loanwords

French loanwords often come with silent letters at the end; they can either be ignored in phonetic outlines, or included as part of orthographic outlines.

| Ending | Pronunciation | Full Orthograhpic | Standard |
|---:|:---|:---|:---|
| ailles | /aɪ/ | `AEUS` | `AEU` |
| ais | /eɪ/ | `AEUS` | `AEU` |
| ait | /eɪ/ | `AEUT` | `AEU` |
| eaux | /oʊ/ | `A*UBGS` | `AU` |
| er | /eɪ/ | `ER` | `AEU` |
| et | /eɪ/ | `ET` | `AEU` |
| ez | /eɪ/ | `ET` | `AEU` |
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

## Syllable Splitting

Syllable splitting refers to how multi-syllable words are split into sequences of strokes. By providing a single standard for splitting syllables, we can make outlines more predictable whilst reducing the dictionary size needed.

### Right Greedy Splitting

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

There are clusters or partial clusters that some users may find difficult to divide purely greedily; there is thus some leniency in the way they are divided:

| Cluster | Greedy | Alternatives |
|---:|:---|:---|
| /stɹ/ | `...*S/SR...` | `...S/STR...` |
| /kstɹ/ (Spelled with x) | `...GT/SR...` | `...*BGS/STR...` |
| /tɹ/ | `...T/SR...` | `.../STR...` |
| /dɹ/ | `...D/SR...` | `.../STKR...` |
| "wr" | `...FB/SR...` | `.../SWR...` |

### Left Bank Glides

When the syllable starts with /j/ or /i/, we can use the `KWR` chord to indicate it; similarly, when a syllable starts with /w/, /u/, or /ʊ/, we can use the `W` key. However, there are cases where a user might try to insert these initials even though they have already been represented by the previous stroke. Whilst they are free to add such outlines, they are not part of the main theory:

- altruistic: `ALT/SRAOU/SWR*EUS/SWREUBG` (alt-ruu-ist-ic, not alt-ruu-wist-ic)
- piano: `PEU/SWRAPB/SWROE` (pi-an-oe, not pi-yan-noe)

### Syllable/Stroke Dropping

Users who wish to take advantage of syllable or stroke dropping may do so, even though they are often based on stress patterns and thus are optional. It is important to still keep using the additional `S-` where applicable to indicate attached strokes to avoid boundary errors.

For words that have 2-stroke write-outs, no strokes can be dropped. 

For words that have 3-stroke write-outs, we can drop the centre stroke after giving any of its finals to the initial of the third stroke, if there is space. Note that 3-stroke write-outs do not necessarily correspond to 3-syllable words. Some examples include:

- similar: `SEUPL/SWREUL/SWRAR` → `SEUPL/SHRAR`
- preposition: `PREP/SWROS/SWREUGS` → `PREP/S*EUGS`
- filament: `TPEUL/SWRAPL/SWREPBT` → `TPEUL/SWR-PLT`

For words that have write-outs with more strokes, syllable dropping is based on stress. Some of these entries will be included in the dictionary, but there are currently no plans (TBC) to include these write-outs for rarer words.

- similarly: `SEUPL/SWREUL/SWRARL/KWREU` → `SEUPL/SHRARL/KWREU`
- prepositional: `PREP/SWROS/SWREUGS/SWRAL` → `PREP/S*EUGS/SWRAL`
- hyperbolical: `HAOEUP/SWR*ERB/SWROL/SWREUBG/SWRAL` → `HAOEUP/SPWOL/SKAL`

### Consonant Greedy

Consonant greedy is an alternative to syllable dropping that reduces the number of strokes per word, without relying on stress. This is accomplished by attempting to squeeze as many consonants or consonant clusters into each stroke as possible, ignoring the vowels between strokes or between consonants on the same side of a stroke, and ignoring any final consonants if the stroke can't accomodate more and the following stroke cannot include it in its initial. For instance:

- similarly: `SEUPL/SWREUL/SWRARL/KWREU` → `SPHEUL/SHREU`
- prepositional: `PREP/SWROS/SWREUGS/SWRAL` → `PREPS/SHO*PBL`
- hyperbolical: `HAOEUP/SWR*ERB/SWROL/SWREUBG/SWRAL` → `HAOEUP/SPW*ERBLG/SWRAL`

In some cases, after putting as many consonants on the left, we are left with no vowels for the thumbs because the splitting point is immediately followed by another consonant. When this occurs, we simply shift the minimal amount of consonants from the left to the right so that we can have a vowel on the thumbs. If the vowel is represented by a no-key chord, that's still okay. For instance:

- cartography: `KR...` doesn't work, so `KART/STKPWRAF/KWREU`

To reduce the number of strokes needed for each word even further, we can make use of the inversions and folds introduced in the previous sections, as well as the `-FR` as M technique. For example:

- similarly: `SPHREURL`
- intricately: `SPWREUBLGT`

### -y Suffix

The "-y" suffix is written using `KWREU` and needs to be memorized explicitly. Here are a few examples of it being used:

- happy: `HAP/KWREU`
- happily: `HAP/SWREUL/KWREU`

## Irregular Briefs

Irregular briefs refer to briefs that do not strictly follow all the core rules listed before. Groups of briefs may still have internally consistent patterns, but they would still have to be explicitly memorized. Work-in-progress.

### Common Briefs

SKP for and, etc...

## Numbers

Cocoa Theory uses the right hand numpad system for numbers. Digits are entered like so:

| Digit | Chord | Digit | Chord | Digit | Chord |
|---:|:---|---:|:---|---:|:---|
| 7 | `#F` | 8 | `#P` | 9 | `#L` |
| 4 | `#FR` | 5 | `#PB` | 6 | `#LG` |
| 1 | `#R` | 2 | `#B` | 3 | `#G` |
| 0 | `#E` | 00 | `#U` | 000 | `#EU` |

While numbers are usually entered digit-by-digit, we can add one to three zeros by using the `EU` keys:

- 40: `#EFR`
- 200: `#UB`
- 8000: `#EUP`

(TBC: More number features)

## Punctuation

With the exception of period and comma, punctuation is done with `KW` on the right and either a phonetic or shape-based memorization hook on the thumb keys and right bank keys.

| Punctuation | Description | Chord |
|---:|:---|:---|
| . | Full Stop / Period | `-FPLT` or `TP-PL` |
| , | Comma | `-RBGS` or `KW-BG` |
| ? | Question Mark | `KW-FPG` or `KW-PL` |
| ! | Exclamation Mark | `KW-PB` or `TP-BG` |
| : | Colon | `KWUF` |
| ; | Semicolon | `KWEUF` |
| ' | Apostrophe | `KW-F` |
| \` | Backtick | `KW-PG` |
| ␣' | Open Single Quote | `KW-P` |
| '␣ | Close Single Quote | `KW-L` |
| ␣" | Open Double Quote | `KW-FP` |
| "␣ | Close Double Quote | `KW-LT` |
| ␣\` | Open Backtick | `KW-FB` |
| \`␣ | Close Backtick | `KW-LS` |
| ( | Open Parenthesis | `KWURP` |
| ) | Close Parenthesis | `KWUPG` |
| [ | Open Bracket | `KWUFP` |
| ] | Close Bracket | `KWUPG` |
| { | Open Brace | `KWURPB` |
| } | Close Brace | `KWUPBG` |
| / | Forward Slash | `KW-RL` |
| \\ | Backslash | `KW-FG` |
| * | Asterisk | `KW-PBLG` |
| @ | At | `KWAT` |
| ␣-␣ | Hyphen | `KW-RBG` |
| - | Joining Hyphen | `KW-FPL` |
| ~ | Tilde | `KW-RPL` |
| ^ | Caret | `KW-RPG` |
| ... | Ellipsis | `KW-BS` |
| & | Ampersand | `KW-FRPBG` or `SKP*` |

## Formatting

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
| Steno Correction | `*` |
| Delete Word | `SW` |
| Return and Capitalize | `R-R` |
| Return and Keep Case | `R-RB` |

## Orthographic System

Work-in-progress.

## Phrasing System

Work-in-progress.