---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
description: My curriculum vitae.
---

<div class="text-center mb-4">
  <a href="{{ '/assets/pdf/cv.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-solid fa-file-pdf"></i> Download CV (PDF)
  </a>
</div>

<div class="ratio" style="--bs-aspect-ratio: 130%;">
  <iframe src="{{ '/assets/pdf/cv.pdf' | relative_url }}" title="Curriculum Vitae" style="width: 100%; height: 100%; border: 1px solid var(--global-divider-color);" allowfullscreen></iframe>
</div>
---
layout: cv
permalink: /cv/
title: CV
nav: true
nav_order: 5
cv_pdf: /assets/pdf/example_pdf.pdf # you can also use external links here
cv_format: rendercv # options: rendercv, jsonresume
description: This is a description of the page. You can modify it in '_pages/cv.md'. You can also change or remove the top pdf download button.
toc:
  sidebar: left
---
