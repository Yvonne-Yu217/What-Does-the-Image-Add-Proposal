# What Does the Image Add?

## Learning to Supplement Existing Descriptions

**CSCI-GA 2271 Computer Vision, Fall 2026**

**Track:** Agent Track · **Format:** Research Project

**Revision:** September 29, 2026

**[Read the proposal (PDF)](proposal.pdf)** · [Edit the LaTeX source](proposal.tex)

### Idea

Given an image and an existing description, can a model add correct, useful facts
without repeating what the reader already knows? For example, if a photograph
shows a red, long-sleeved shirt and the text already says “a red shirt,” a useful
addition would be “long-sleeved.”

We propose to learn from examples showing what an existing description leaves
out, and compare this approach with ordinary captioning and full-image prompting.
Versions with and without bounding boxes will help us understand whether region
guidance is useful.
The main study will keep the object specified in text; allowing the model to
choose the object as well will be a separate extension. Natural descriptions,
factual errors, independent question-answering utility, transfer, and total
computational cost will determine whether the approach is useful.

### Planned questions

1. Does paired-state training improve missing-fact recovery while reducing repetition?
2. Does explicit region guidance help beyond an equally trained full-image model?
3. Do improvements generalize to natural text and benefit independent image questions?

The document presents the research motivation, hypotheses and planned experiments.
It makes no empirical performance claims or guarantees that a method will succeed.

### Course requirements

Prepared against the [official project page](https://www.sainingxie.com/cv-fall2026/project/),
read September 29, 2026. The PDF covers the idea, significance, methods, evaluation
metrics, expected deliverables, risks, preliminary timeline, computing resources,
and track/format declaration.

The proposal must be submitted as a PDF through Gradescope. The 4–9-page range
applies to the **final research report**, excluding references; the final Agent
Log is also excluded. The course page specifies no proposal page limit.
This repository publishes the document and does not submit it to Gradescope.

The proposal remains without author names for team discussion. The course normally
requires a team of 2–5 students, and the final report must list individual
contributions. Every member must be able to explain the submitted work.

This is a **proposal-only repository**. The separate research repository retains
implementation history and experimental records; this document repository does
not replace the incremental code history required for the final project.
No datasets, checkpoints, or experiment code are bundled here.

### Build

Use a LaTeX distribution with `pdflatex` and the standard packages declared in
`proposal.tex`:

```sh
pdflatex -interaction=nonstopmode -halt-on-error proposal.tex
pdflatex -interaction=nonstopmode -halt-on-error proposal.tex
```

Two passes resolve references. The source may also be uploaded to Overleaf.
The proposal is AI-assisted writing under the declared Agent Track. Team review
and final submission remain part of the course workflow.
