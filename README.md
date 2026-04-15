# guidelines_writing_papers

My personal guidelines writing papers - things that come up again and again. Crisp and effective writing is hard, and applying these is a constant struggle, this is perfectly normal :) .

Suggest extra guidelines in issues.

I used to say that maybe, one day, a linter could be implemented for some of these categories - now this can just be fed into AI to ask it to enforce these guidelines :) .

This is integrated as a full Agentic AI workflow at: https://github.com/jerabaul29/2026_template_paper_agentic_ai .

# About the form / presentation of the writing [F]

## Meta [F:X]

- **F:X0**: use a version control system to track changes: ideally git (possibly git + overleaf), at least overleaf with track changes when several authors edit the same document.
- **F:X1**: prefer using LaTeX whenever possible.
- **F:X2**: use a spellchecking tool, and ideally a LLM language checking tool too. This can be done either using a LLM tool built into your editor (as a LSP for code / vim / helix / emacs etc, or as the writefull extension on overleaf), or by just copy pasting the tex content into copilot or chat-gpt and asking with proper prompt engineering to make the text better for a scientific paper. Remember that (anno 2025 at least) LLMs are not good at generating content (they will often / there is a risk that they lie, hallucinate, make up stuff, mix things up, etc), but they are very good at taking poorly written text and making it into nicely written text, keeping the same ideas. This is how LLMs should be used.
- **F:X3**: when doing a major revision (for example, following a review round), generate a diff between the present and previous version, using ```latexdiff``` or similar.
- **F:X4**: be consistent also in the source file of the manuscript; for example, use newlines / blank lines consistently between sections, around figures / tables / headings, etc.
- **F:X5**: have "major versions" (typically corresponding to the versions you upload to preprint servers and / or send to the journal after different review rounds) into self contained folder in e.g. overleaf; this way, it is easy to quickly compare, look back at a version, do a diff, re-compile an old version, etc. Have each of these folders self contained and compiling on its own. This way, there are no inter-dependencies and you can re-compile easily in the exact state of an old submitted version; i.e., an organization like:
```
- v1_arxiv_first_submission
   |- figs
   |    |- my_fig_1.png
   |    |- my_fig_2.png
   |- style.sty
   |- bibliography.bib
   |- main.tex
- v2_journal_first_submission
   |- figs
   |    |- my_fig_1.png
   |    |- my_newfig_2.png
   |- style.sty
   |- bibliography.bib
   |- main.tex
- v3_journal_second_submission
   |- figs
   |    |- my_modifiedfig_1.png
   |    |- my_newfig_2.png
   |- style.sty
   |- bibliography.bib
   |- main.tex
```

## General [F:G]

- **F:G0**: Keep It Stupid Simple. Make simple things simple and complicated things understandable. Reduce to simple ideas / first principles, even if this requires breaking things down in several steps.
- **F:G1**: avoid overly heavy boilerplate. There has been a tradition for "writing everything assuming no backgroud knowledge" in some research fields, and as a consequence some articles end up containing lots of boilerplate. Try to refer to reference sources instead, and explain the main lines, but not the details, of background information that has been described again and again in the past.
- **F:G2**: if possible, avoid repetitions of ideas and discussions; however, consider context: if the paper is long, it may be necessary to refresh ideas discussed above or mention that things will be discussed further down ("as discussed above" or "see below")
- **F:G3**: Be brief, be bright, be gone: try to convey the exact message you want to convey as effectively as possible. A shorter paper is easier to read, understand, etc. You goal is to convey your message, as clearly and effectively as possible. Do not waste your reader's time with useless details and un-necessary information.
- **F:G4**: Have a clear story / red line.
- **F:G5**: Try to be specific / technically to the point, without being pedantic; in particular, avoid pedantic formulations, unnecessary details and "poetic" adjectives, be terse and easy to read, avoid being "poetic".
- **F:G6**: use a consistent, well defined, non ambiguous nomenclature. If necessary, define specific nomenclature that helps to explain and understand the key points. Disambiguate concepts with appropriate terminology.
- **F:G7**: do not speculate / come with ungrounded or bold statements / discuss "tricky" questions more than is necessary for the science you want to convey in the present paper. Be "strategic" and avoid un-necessary discussions that are not needed for the main scientific message of the present paper - this only creates issue during the review process, and may make the paper age less well. Be focused on the scientific message and goal. Relatedly, avoid scope creep: resist the urge to answer too many questions in a single paper; a focused paper with a clear contribution is easier to publish and more impactful than a broad one that tries to cover everything.

## Title [F:T]

- **F:T1**: the title is the most-read part of the paper — make it count. It should be concise, specific, and informative: a reader should immediately understand the topic and scope of the paper from the title alone.
- **F:T2**: make the title searchable: include the key technical terms that readers in the field would use when searching for papers on this topic.
- **F:T3**: avoid vague or clickbait-style titles (e.g., "A novel approach to..."), and avoid overly long titles with excessive qualifiers. Aim for something crisp that stands on its own.

## Abstract [F:Ab]

- **F:Ab1**: the abstract is often the only part people read — it must be self-contained and fully convey the paper's contribution, even without reading the rest. Define all abbreviations used in it; do not assume the reader has read anything else.
- **F:Ab2**: a good abstract typically covers: i) context / motivation (why this matters), ii) problem statement (what is being addressed), iii) approach (what was done), iv) key results (what was found, with concrete numbers if possible), v) conclusion / implications (why this is significant).
- **F:Ab3**: the abstract should state the key result explicitly and concretely — avoid vague statements like "results are promising". Say what was achieved and by how much.

## Style [F:S]

- **F:S0**: avoid strong adjectives / hyperboles, especially if vague: i.e. avoid qualificators like "very", "the most", etc, if not there is a clear factual reason for this (for example, comparing a few cases, and finding that one is "the most" of them is fine; saying that some diffuse / unspecific "thing" is "the most", is not fine).
- **F:S1**: use present tense, avoid complex present / future / past mix in a paper: i.e., write "we show", "we do", etc.
- **F:S2**: write short sentences, with simple structure: "Subject, Verb, Complement". Keep 1 idea per sentence. Cut long sentences into shorter sentences.
- **F:S3**: use consistent terminology. In literature, we like using different words to describe the same "thing", to avoid heavy, ugly repetitions. In scientific writing, the simpler the better, and a given "thing" should be referred consistently by the same word(s), even if this leads to repetitions.
- **F:S4**: write in "terse, professional" English: avoid spoken English, familiar expressions.
- **F:S5**: use simple English, avoid complex / unusual words: most of your readers will not be native English speakers, so the simpler vocabulary you use, the easier to read.
- **F:S6**: equations are part of the sentence: make sure that they end with a ".", or if with a ",", that the sentence continues on the next line.
- **F:S7**: avoid passive form; this is harder to read and understand, and more verbose than simple direct form.
- **F:S8**: avoid double negation; this is very confusing to read.
- **F:S9**: if relevant, explain important points in several ways, using different and complementary perspectives on the problem. This is useful for the reader to understand the point, and is a way to hammer in key points in a constructive way.
- **F:S10**: make sure that the information and sentences are well grouped into paragraphs, and that there are transitions between these. Nothing should "hang in the air", there should be logical transitions so the text flows well. Highlight these transitions as needed (using transition words like "as a consequence", "therefore", "by contrast", "however", etc).
- **F:S11**: use SI units consistently, and format numbers and units carefully: use a non-breaking space between a number and its unit, use consistent decimal separators, and avoid ambiguous notations. In LaTeX, the `siunitx` package is recommended for this.

## LaTeX [F:L]

- **F:L1**: use version control for the LaTeX files: either git, or overleaf + git.
- **F:L2**: if using overleaf with a pro account, remember to enable Writeful LLM language advices.
- **F:L3**: use the right kind of citation: generally `\citep` (cite with parenthesis), or `\citet` (cite in text), otherwise `\cite`.
- **F:L4**: treat the tex files like code: be consistent, have spaces and good indentation.

## Figures [F:F]

- **F:F1**: have detailed captions for figures (and Tables). Ideally, it should be possible for someone with knowledge of the field to read just the abstract, conclusion, and figures + captions, and get a good understanding of the paper and results. Have detailed captions that have all the information needed to read and understand the figures without the need to read the text fishing for information, even if this results in long captions. Also have a short word of discussion (the "why" / "what this shows"), to explain what this figure shows and what its point is.
- **F:F2**: make sure the figures are easy to read: large enough font, not overcrowded etc. Make sure to use good axis labels, lines labels, to take advantage of colors, markers, sizes, background shade, etc. Also verify that the figures remain readable when printed in black and white, as this is still common in many venues.
- **F:F3**: make sure all figures and tables are referred to in the text.
- **F:F4**: make good use of color / style / bold or italic to highlight what you want to show in the figure and make it easy to understand; think carefully about what message(s) you want the figure to contain.
- **F:F5**: use colorblind-friendly palettes (e.g., Okabe-Ito, viridis, or similar perceptually uniform palettes). Avoid relying on red/green contrast alone to convey information. This ensures the figures are accessible to a wider audience.

## Appendix [F:A]

- **F:A1**: use Appendixes for boilerplate but necessary content (for example, following request by reviewer).
- **F:A2**: use Appendixes to present technical details that are important but would otherwise disturb the flow of the reading.
- **F:A3**: if releasing code / data (hopefully doing it!), consider having a specific Appendix describing these and linking to the resources, so that this "stands out" and is not just hidden deep in the main article body.

## Methodology [F:M]

- **F:M1**: ideally, the methodology section should be enough to reproduce the methodology of the paper. In practice, it may be hard to condense many technical details in a methodology section. If this is the case, consider releasing code and data as supplementary materials.
- **F:M2**: if the methodology is better explained with a figure, create a figure to illustrate.
- **F:M3**: if there are many metaparameters used in the methodology, summarize these in a table.

## Supplementary materials [F:U]

- **F:U1**: if relevant, use supplementary materials.
- **F:U2**: make sure that supplementary materials are easy to find and high visibility: provide clear direct links to these in the paper / on the github repository. Consider having an appendix "External links" summarizing all links at the end of the paper.
- **F:U3**: try to release supplementary materials on common well known platforms. For examples, if releasing a video, it will be seen a lot more if it is released on youtube (with proper title, caption, and link from the paper) in addition to being provided as a .zip, than if it is only released as a .zip alongside the paper on the publisher website.

## References [F:R]

- **F:R1**: use a tool for generating the references; at least using bibtex and a bibliography .bib file (do not embedd the bibliographic entries into the manuscript, except at the last production step if required by the journal); ideally the .bib file could be exported from Zotero or similar, if not, the references can be exported individually from GScholar or similar (click on article -> all versions -> choose the relevant one and click "cite" -> BibTex).
- **F:R2**: check for references duplicates.
- **F:R3**: verify that all references are accurate: check that DOIs are valid, that the journal / venue / year / authors are correct, and that no fields are missing or garbled (a common issue when importing from GScholar). Do not trust bibtex entries blindly.

## Abbreviations [F:B]

- **F:B1**: define the abbreviations the first time they are met, like: "Deep Reinforcement Learning (DRL)". After that, the DRL abbreviation can be used. Note that it may be a good idea to re-define the abbreviations in critical parts of the text, i.e. the conclusion, so that it can be read by itself without the need to look through the whole paper looking for their meaning. The abstract should also be self-contained: re-define all abbreviations used there, since the abstract is often read in isolation (e.g., in search results or databases).

## Impact [F:I]

- **F:I0**: make sure that the manuscripts are easy to find without the need to go through paywalls: release the latest preprints and the postprints on ArXiv and ResearchGate under a permissive license.
- **F:I1**: make it easy for others to re-use the work. Release code, scripts, post processing snippets etc on github or similar, with detailed readme and user manuals. Make sure the code is runnable (ideally, provide a conda env and or even better a container image of some sort). If the data are small enough, host them on github too (possibly with git-lfs), so that the scripts can be run as is after a git-clone to reproduce the figures. Consider saying / writing that reasonable support will be provided through the issue tracking system on the github (or similar) repository.

## Publication [F:P]

- **F:P1**: release the preprint on ArXiv / ResearchGate as soon as it is ready; this way this i) immediately starts diffusing the ideas and concepts to the community, ii) establishes a public record and timestamp (to claim originality / first about the ideas). This is especially important as peer review can take months or years depending on the journal. Make sure to share the links / authorship claim links with all co-authors.
- **F:P2**: update the ArXiv / ResearchGate manuscripts as new versions get rolled out, until the last "postprint" (i.e. last preprint after the review process has been done) is uploaded. Even consider updating the postprint after publication of a peer reviewed paper if relevant. Both ArXiv and ResearchGate can store multiple updated versions of the same manuscript and make it easy to browse through versions.
- **F:P3**: if relevant, consider publishing in traditional peer reviewed literature. Things to be aware of are i) costs ii) delays iii) copyrights. Usually, all journals are legally forced to accept that the authors release preprint and postprints as they want (since usually authors have full legal ownership of their preprint and postprint, as long as the journal has not done any work on these). This should be the case as long as no editing done by the journal (usually happening after the files are delivered for production) is included in the publicly released materials. I.e., a proofs edited by the journal is not allowed to release, but a postprint should be allowed to release.
- **F:P4**: have an advertisement cycle on linkedin / twitter etc that follows the publication process. Typically, it is useful to have i) one round of advertisement when the first preprint is released (with a notice, if relevant, that code + data will be released open upon publication in the peer reviewed literature), ii) one round of advertisement when the paper is published if so (with link to the code and data). This is redundant, but since there are usually many months of review between i) and ii), this is quite acceptable. Make sure to link to the preprint / code / data, tag co-authors, and include an eye catching summarizing picture. I would recommend linking to ResearchGate rather than ArXiv, since ResearchGate is a social network, so having a manuscript there with a lot of reads will snowball and increase its spreading further. Consider releasing during mid day Europe time in the middle of the week, to reach as many people as possible globally.
- **F:P5**: try to avoid dead links at any step of the release / publication process. I.e. if code / data are kept private until a paper publication in peer review, make sure to i) create all the relevant data and code repositories, keeping them empty, with a notice that "code and data will be released upon publication in the peer reviewed literature", ii) link to these placeholders from the manuscript so there is no dead link. You can still iii) have a private "shadow repository" for revising and working on the code and data during the review process. When writing a post, remember to i) include an eye catching figure, that you describe briefly (saying what the main point / "thing to see" is) in the post, ii) start the post by a good catchphrase that explains why this is important and useful, iii) write something that is understandable, and puts into context, iv) write clearly what the novelty is v) have all relevant links (ResearchGate, ArXiv) included, vi) tag the relevant co-authors, vii) use keywords with #. Make sure to share the link with all co-authors by email.
- **F:P6**: make sure to release all code and data, and make these very visible / accessible.

## Follow up [F:O]

- **F:O1**: offer to provide reasonable support on the github repository associated with the paper.
- **F:O2**: if some typos / minor mistakes are found, issue a notice at the bottom of the readme on the github of the paper. Consider updating the ArXiv / ResearchGate versions. If the typo is small, it is generally not worth issuing a correction at the publisher - this is too much work, and the original paper will usually not get updated, it will just get a correction notice.

## Response to reviewers [F:V]

- **F:V1**: address every single point raised by every reviewer, without exception. Even if you disagree, acknowledge the point and explain your reasoning clearly and respectfully.
- **F:V2**: structure the response letter clearly: quote each reviewer comment, then provide your response, and indicate what changes were made to the manuscript (with page / line numbers if possible).
- **F:V3**: be respectful and constructive, even when reviewers are wrong or their comments are unclear. Thank them for their time and their feedback, including negative feedback.
- **F:V4**: when making changes to the manuscript in response to a review, make these changes clearly visible (e.g., highlighted in the revised manuscript, or described precisely in the response letter). Use `latexdiff` or similar to generate a diff for the editor.
- **F:V5**: if you disagree with a reviewer comment and choose not to make the suggested change, explain your reasoning clearly and provide supporting arguments or references. This is perfectly acceptable.

# About the content of the writing and the science contained [S]

## Introduction [S:I]

- **S:I1**: structure the introduction as a funnel: start broad (the general field and why it matters), progressively narrow to the specific problem being addressed, and end with a clear statement of the paper's contributions and structure.
- **S:I2**: state the contributions of the paper explicitly and concisely, ideally in a dedicated paragraph or bulleted list near the end of the introduction. The reader should know exactly what is new in this paper before moving on.
- **S:I3**: cite and situate the work relative to the most relevant prior art. Do not over-cite (padding) or under-cite (missing important related work). The goal is to give the reader the context needed to appreciate the novelty and significance of the contribution.
- **S:I4**: explain the structure of the manuscript at the end of the introduction: for example (adapt as needed): "In the following, we describe ... in section ... . Then we discuss ... in section ... . Finally, we discuss ... in section ... ."

## Results [S:R]

- **S:R1**: present results clearly and objectively. Separate the presentation of results from their interpretation: first show what was found, then discuss what it means.
- **S:R2**: always quantify results: give numbers, uncertainties, effect sizes, or statistical significance as appropriate. Avoid qualitative-only descriptions of quantitative results (e.g., "the method performs better" — better by how much?).
- **S:R3**: compare against appropriate baselines. Make sure that the baselines are fair and well-described, and that the comparison is meaningful (same conditions, same metrics, etc.).
- **S:R4**: be honest and complete about results that did not go as expected or that show limitations of the method. Selective reporting undermines scientific integrity and tends to be caught during review anyway.

## Discussion [S:D]

- **S:D1**: interpret results in the light of the existing theory and literature: what do the results confirm, contradict, or add to what was already known?
- **S:D2**: discuss the limitations of the work honestly and explicitly. Every study has limitations; acknowledging them increases credibility and helps the reader calibrate how far the conclusions can be generalized.
- **S:D3**: suggest concrete directions for future work, grounded in the limitations and open questions identified in the paper. Avoid vague statements like "future work will explore this further"; be specific about what remains to be done and why.

## Conclusion [S:N]

- **S:N1**: the conclusion should succinctly summarize the key findings and contributions of the paper. It should not introduce new material or arguments.
- **S:N2**: restate the main take-away message in plain language: what does this paper establish, and why does it matter? A reader who reads only the abstract and conclusion should come away with a correct and complete high-level understanding of the paper.
- **S:N3**: define / recall abbreviations used in the conclusion, as it is often read in isolation (similar to the abstract).

## Theory [S:T]

- **S:T1**: provide a clear overview of the existing theory; if the theory is lacking / partial / does not match 100% an experimental or numerical work, this is perfectly fine, but this should be made clear: this way, readers are aware of what theoretical development are lacking and are good directions for future work.
- **S:T2**: make it clear when a theory is used outside of its strict domain of validity, and how so; this may be fine to do, as many theories can be extrapolated a bit, but this should be made clear.
- **S:T3**: make it clear what is an axiom / a fundamental law of nature (and which axiom(s) law(s) of nature are relevant), vs. what is a consequence derived from an axiom / a fundamental law of nature (and which axiom(s) law(s) of nature are used as starting points, and what the domain of validity of the derived result is), vs. what is empirical or semi-empirical fact, vs. what is commonly accepted but not the direct formal consequence of an axiom or law of nature, vs. what is speculation.

## Crediting [S:C]

- **S:C1**: make sure that you credit relevant previous works and sources of pre-existing ideas.
- **S:C2**: make it clear what ideas are novel and introduced by your paper, and what is repeating / re-formulating previous ideas.
- **S:C3**: credit not only papers, but also code frameworks, libraries, dataset, discussions, grey literature, etc, that are relevant.
- **S:C4**: credit (either inviting as co-authors, or in acknowledgement) third parties that have been key to make the paper possible: lab technicians / oceanographic research ships / grant officers.
- **S:C5**: define authorship carefully and early, in agreement with all co-authors. Consider using the CRediT (Contributor Roles Taxonomy) framework to specify each author's contribution explicitly (e.g., Conceptualization, Methodology, Software, Writing, etc.). This avoids misunderstandings and is increasingly required or encouraged by journals.
- **S:C6**: if using LLMs, acknowledge / disclose it in the Acknowledgment part or similar. This is both to be transparent, and also to be proactive in case LLM-detection software is run on your manuscript and gives a positive hit at some point in the future. A typical standard acknowledgement / disclosure paragraph can be along the lines of:
    > "We have used LLM-powered tools to improve language quality and correctness. All the scientific content is the result of the work of the authors, and the authors checked and quality controlled all LLM-produced language edits."
