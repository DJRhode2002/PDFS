# PDFS

## Carburettor Icing Training &amp; Exam System

`index.html` is a self-contained (no external dependencies) web application built from the PDFs in
this repository:

* **Study phase** &ndash; the full basic pilot training manual (`Carb Icing Training Manual.pdf`),
  followed by a warning box and a **Start Exam** button.
* **Exam lockout** &ndash; starting the exam asks for confirmation, then removes the manual from the
  DOM and intercepts browser back-navigation so it cannot be reached again without reloading.
* **Randomised exam** &ndash; drawn from the 240 questions in
  `Carb Icing Training Exam Questions Master.pdf`:
  * Section 1 &ndash; 50 random general questions (no chart).
  * Section 2 &ndash; 10 random chart questions, with the chart pinned to the top of the viewport.
  * Section 3 &ndash; 10 random advanced scenario questions, with the chart pinned to the top of the
    viewport.
* **Interactive UI** &ndash; multiple-choice radio inputs and a toggleable **Show Answer** button per
  question revealing the correct option and, where the source provides one, the explanation.

The Carburettor Icing-Probability Chart (`PDF.pdf`) is embedded as a base64 image.

Open `index.html` in any modern browser; no build step or server is required.
