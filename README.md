# PDFS

## Carburettor Icing Training &amp; Exam System

`index.html` is a self-contained (no external dependencies) web application built from the PDFs in
this repository. Open it in any modern browser &ndash; there is no build step and no server required.

### Workflow

1. **Study phase** &ndash; the full basic pilot training manual (`Carb Icing Training Manual.pdf`),
   followed by a warning box and the **I Have Read the Material &mdash; Start Exam Now** button.
2. **Exam lockout** &ndash; starting the exam asks for confirmation, then removes the manual from the
   DOM and intercepts browser back-navigation, so it cannot be reached again without reloading.
3. **Randomised exam** &ndash; drawn from the 240 questions in
   `Carb Icing Training Exam Questions Master.pdf`:
   * Section 1 &ndash; 50 random general questions (no chart).
   * Section 2 &ndash; 10 random chart questions, with the chart pinned to the top of the viewport.
   * Section 3 &ndash; 10 random advanced scenario questions, with the chart pinned to the top of the
     viewport.
4. **Sitting the exam** &ndash; multiple-choice radio inputs only. No answers, marks or feedback are
   revealed while the exam is in progress; a single **Submit Exam for Grading** button sits at the
   bottom of the paper.
5. **Grading** &ndash; each section is scored independently and combined by weight:

   | Section | Weight |
   | --- | --- |
   | Section 1 &ndash; General | 50% |
   | Section 2 &ndash; Chart | 25% |
   | Section 3 &ndash; Advanced | 25% |

   To **pass**, a candidate needs **at least 80% in every individual section _and_ an overall
   weighted score of 80% or higher**. Unanswered questions are marked incorrect.
6. **Review screen** &ndash; a PASS/FAIL banner with the overall weighted percentage, a per-section
   score breakdown, and an itemised review of every question showing the candidate's answer, the
   correct answer and the reasoning.

Where the source question bank records an answer without a written explanation (the Section 1
general questions), the review states the correct answer and refers the candidate back to the
relevant manual topic rather than inventing reasoning.

The Carburettor Icing-Probability Chart (`PDF.pdf`) is embedded as a base64 image.
