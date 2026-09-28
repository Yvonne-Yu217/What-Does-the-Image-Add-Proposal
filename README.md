# What Does the Image Add?

## Text-Conditioned Visual Detail Completion

**CSCI-GA 2271 Computer Vision, Fall 2026**

**Track:** Agent Track · **Format:** Research Project

**Revision:** September 29, 2026

**[Read the two-page proposal (PDF)](proposal.pdf)** · [Edit the LaTeX source](proposal.tex)

### Project in one paragraph

Given an image, an existing description, and a specified object, we ask whether a
vision-language model can add a correct, useful detail that the text does not
already convey. Completed experiments support improved descriptions of objects
in human-provided boxes. The proposed next stage explicitly conditions generation
on existing text and evaluates missing-detail recovery, factual errors, strong
full-image alternatives, automatic localization, and independent question-answering
utility. Cross-domain reliability and publication-level novelty remain unproven.

### What changed

- The method now centers on grounded generation and text-conditioned completion,
  following failures of sentence selection and transfer.
- Completed E100 results are separated from the failed E101 transfer gate and
  pending E103/E107 evidence. Automated scores are not called human factual accuracy.
- Matched-data text-conditioning ablations and equally trained full-image controls
  are planned to distinguish the proposed mechanism from fine-tuning alone.
- Practical utility and novelty are separate requirements; neither is claimed from
  ordinary region captioning or a proxy score alone.

### Course requirements

Prepared against the [official project page](https://www.sainingxie.com/cv-fall2026/project/),
read September 29, 2026. The PDF includes the research question, significance,
method, evaluation metrics, expected deliverables, risks, preliminary timeline,
computing resources, and an explicit track/format declaration.

The course asks for proposal submission as a PDF through Gradescope. The 4–9-page
range applies to the **final research report**, excluding references; the final
Agent Log is also excluded. The course page specifies no proposal page limit.
This repository publishes the document and does not submit it to Gradescope.

This public proposal intentionally contains no author names. The final course
report must attribute individual contributions, and every team member must be
able to explain the submitted work.

### Evidence provenance

Results reflect research repository commit
[`cf871d6ae94c170a896a7bf1e708beeb0027a31a`](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/tree/cf871d6ae94c170a896a7bf1e708beeb0027a31a).
This is a dated snapshot, not a claim that queued HPC jobs have since finished.

- [E100: completed grounded phrase generation](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/blob/cf871d6ae94c170a896a7bf1e708beeb0027a31a/research/E100_GROUNDED_PHRASE_GENERATOR.md)
- [E101: failed cross-domain primary gate](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/blob/cf871d6ae94c170a896a7bf1e708beeb0027a31a/research/E101_CROSS_DOMAIN_GROUNDED_PHRASE.md)
- [E103: interim relative-to-text result](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/blob/cf871d6ae94c170a896a7bf1e708beeb0027a31a/research/E103_RELATIVE_T_PHRASE_NOVELTY.md)
- [E107: registered text-conditioned method](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/blob/cf871d6ae94c170a896a7bf1e708beeb0027a31a/research/E107_T_CONDITIONED_RESIDUAL_GENERATOR.md)
- [E109: independent QA data audit preparation](https://github.com/Yvonne-Yu217/CSGA2271_Project_Yvonne_Yu/blob/cf871d6ae94c170a896a7bf1e708beeb0027a31a/research/E109_VG_HUMAN_QA_PREFLIGHT.md)

This is a **proposal-only distribution repository**. The research repository
retains the incremental implementation history and experimental records required
for the final project; a new document repository does not replace that history.
No datasets, checkpoints, or experiment code are bundled here.

### Build

Use a LaTeX distribution with `pdflatex` and the standard packages declared in
`proposal.tex`:

```sh
pdflatex -interaction=nonstopmode -halt-on-error proposal.tex
pdflatex -interaction=nonstopmode -halt-on-error proposal.tex
```

Two passes resolve references. The source may also be uploaded to Overleaf.
The PDF is AI-assisted writing under the declared Agent Track; its empirical
claims were checked against the pinned reports. Human team review remains part
of preparing the final course submission.
