---
tags:
  - technical
  - software
  - infrastructure
  - PDF-processing
  - language-model
---

We need to have a pipeline to consume an arbitrary report that has sections in it. And we need to be able to understand it page by page because it's a PDF. And PDFs don't render very well. We're using tools like Pandas, which is a library from Pandoc, which allows us to manipulate any document files including PDF. We're rendering those to an image as an intermediary. And then we're using things like Tesseract to extract the text roughly from these pictures. And then we're going to use a local language model to describe that information and help us classify the pages. And then what we end up with is effectively a machine-generated table of contents describing what every page in the PDF is. And from there, we can use another language model to then ingest those in great detail and create our graph memory terms from each of the pages that we care about.

---

## Audio File Information

- **Source File:** text_extract_pdf_process-may-14-2025.m4a
- **Duration:** 1:05
- **Transcribed:** 2025-05-15 12:15:37
