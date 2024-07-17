# guidelines_writing_papers

My personal guidelines writing papers - things that come up again and again. Crisp and effective writing is hard, and applying these is a constant struggle, this is perfectly normal :) .

Suggest extra guidelines in issues.

## Meta [X]

- **X0**: use a version control system to track changes: ideally git (possibly git + overleaf), at least overleaf with track changes when several authors edit the same document.
- **X1**: prefer using LaTex whenever possible.
- **X2**: use a spellchecking tool, and ideally a LLM language checking tool too.
- **X3**: when doing a major revision (for example, following a review round), generate a diff between the present and previous version, using ```latexdiff``` or similar.
- **X4**: be consistent also in the source file of the manuscript; for example, use newlines / blank lines consistently between sections, around figures / tables / headings, etc.

## General [G]

- **G0**: Keep It Stupid Simple. Make simple things simple and complicated things understandable. Reduce to simple ideas / first principles, even if this requires breaking things down in several steps.
- **G1**: avoid overly heavy boilerplate. There has been a tradition for "writing everything assuming no backgroud knowledge" in some research fields, and as a consequence some articles end up containing lots of boilerplate. Try to refer to reference sources instead, and explain the main lines, but not the details, of background information that has been described again and again in the past.
- **G3**: Be brief, be bright, be gone: try to convey the exact message you want to convey as effectively as possible. A shorter paper is easier to read, understand, etc. You goal is to convey your message, as clearly and effectively as possible. Do not waste your reader's time with useless details and un-necessary information.
- **G4**: Have a clear story / red line.
- **G5**: Try to be specific / technically to the point, without being pedantic; in particular, avoid pedantic formulations, unnecessary details and "poetic" adjectives, be terse and easy to read, avoid being "poetic".
- **G6**: use a consistent, well defined, non ambiguous nomenclature. If necessary, define specific nomenclature that helps to explain and understand the key points. Disambiguate concepts with appropriate terminology.

## Style [S]

- **S0**: avoid strong adjectives / hyperboles, especially if vague: i.e. avoid qualificators like "very", "the most", etc, if not there is a clear factual reason for this (for example, comparing a few cases, and finding that one is "the most" of them is fine; saying that some diffuse / unspecific "thing" is "the most", is not fine).
- **S1**: use present tense, avoid complex present / future / past mix in a paper: i.e., write "we show", "we do", etc.
- **S2**: write short sentences, with simple structure: "Subject, Verb, Complement". Keep 1 idea per sentence. Cut long sentences into shorter sentences.
- **S3**: use consistent terminology. In literature, we like using different words to describe the same "thing", to avoid heavy, ugly repetitions. In scientific writing, the simpler the better, and a given "thing" should be referred consistently by the same word(s), even if this leads to repetitions.
- **S4**: write in "terse, professional" English: avoid spoken English, familiar expressions.
- **S5**: use simple English, avoid complex / unusual words: most of your readers will not be native English speakers, so the simpler vocabulary you use, the easier to read.
- **S6**: equations are part of the sentence: make sure that they end with a "."., of if with a ",", that the sentence continues on the next line.
- **S7**: avoid passive form; this is harder to read and understand, and more verbose than simple direct form.
- **S8**: avoid double negation; this is very confusing to read.
- **S9**: if relevant, explain important points in several ways, using different and complementary perspectives on the problem. This is useful for the reader to understand the point, and is a way to hammer in key points in a constructive way.

## Figures [F]

- **F1**: have detailed captions for figures (and Tables). Ideally, it should be possible for someone with knowledge of the field to read just the abstract, conclusion, and figures + captions, and get a good understanding of the paper and results. Have detailed captions that have all the information needed to read and understand the figures without the need to read the text fishing for information, even if this results in long captions. Also have a short word of discussion (the "why" / "what this shows"), to explain what this figure shows and what its point is.
- **F2**: make sure the figures are easy to read: large enough font, not overcrowded etc. Make sure to use good axis labels, lines labels, to take advantage of colors, markers, sizes, background shade, etc.
- **F3**: make sure all figures and tables are referred to in the text.
- **F4**: make good use of color / style / bold or italic to highlight what you want to show in the figure and make it easy to understand; think carefully about what message(s) you want the figure to contain.

## Appendix [A]

- **A1**: use Appendixes for boilerplate but necessary content (for example, following request by reviewer).
- **A2**: use Appendixes to present technical details that are important but would otherwise disturb the flow of the reading.
- **A3**: if releasing code / data (hopefully doing it!), consider having a specific Appendix describing these and linking to the resources, so that this "stands out" and is not just hidden deep in the main article body.

## Methodology [M]

- **M1**: ideally, the methodology section should be enough to reproduce the methodology paper. In practice, it may be hard to condense many technical details in a methodology section. If this is the case, consider releasing code and data as supplementary materials.
- **M2**: if the methodology is better explained with a figure, create a figure to illutrate.
- **M3**: if there are many metaparameters used in the methodology, summarize these in a table.

## References [R]

- **R1**: use a tool for generating the references; at least using bibtex and a bibliography .bib file (do not embedd the bibliographic entries into the manuscript, except at the last production step if required by the journal); ideally the .bib file could be exported from Zotero or similar, if not, the references can be exported individually from GScholar or similar (click on article -> all versions -> choose the relevant one and click "cite" -> BibTex).
- **R2**: check for references duplicates.

## Abbreviations [B]

- **B1**: define the abbreviations the first time they are met, like: "Deep Reinforcement Learning (DRL)". After that, the DRL abbreviation can be used. Note that it may be a good idea to re-define the abbreviations in critical parts of the text, i.e. the conclusion, so that it can be read by itself without the need to look through the whole paper looking for their meaning.

## Impact [I]

- **I0**: make sure that the manuscripts are easy to find without the need to go through paywalls: release the latest preprints and the postprints on ArXiv and ResearchGate under a permissive license.
- **I1**: make it easy for others to re-use the work. Release code, scripts, post processing snippets etc on github or similar, with detailed readme and user manuals. Make sure the code is runnable (ideally, provide a conda env and or even better a container image of some sort). If the data are small enough, host them on github too (possibly with git-lfs), so that the scripts can be run as is after a git-clone to reproduce the figures. Consider saying / writing that reasonable support will be provided through the issue tracking system on the github (or similar) repository.

