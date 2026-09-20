# Day 5 speaker notes — Files and document ingestion

## 01 — Files and document ingestion

Welcome to Day 5. Real work usually arrives in files, not inside our Python code. Today we will take a customer FAQ and an IT handbook through a clear pipeline: read, validate, extract, process, and write.

## 02 — Today’s outcome

By the end, you can read a text file, pull text from a PDF, save a result, and explain common file failures in plain language. You will also know which checks can run locally before we spend money on an AI call.

## 03 — The real workflow

A useful document tool has five stages. It reads bytes from a file. It validates what arrived. It extracts usable text. It processes that text. Finally, it writes an output that another person or system can use.

## 04 — Start with trust

Before opening a document, ask where it came from, who owns it, and whether its contents may be sent to an outside provider. A file being technically readable does not mean we are allowed to process it.

## 05 — A path points to a file

A path is the file’s address. Relative paths can break when we run a command from another folder. These labs build paths from `__file__`, so the scripts can find their data from the repository root.

## 06 — Reading text safely

For a normal text document, we open the file in read mode and name the encoding. UTF-8 is a common encoding that tells Python how stored bytes become characters. The `with` block closes the file even if later code fails.

## 07 — Validate before processing

Check that the path exists, the extension is allowed, and the file is within a size limit. These checks give fast and clear failures. They also stop unsupported or unexpectedly large inputs before an expensive step.

## 08 — A PDF is a container

A PDF can hold selectable text, pictures, fonts, and page instructions. `pypdf` reads the pages and extracts stored text. It does not understand every visual layout the way a person does.

## 09 — Text PDF or scanned PDF?

If you can select words in a PDF viewer, the file probably contains text. A scanned PDF may contain only page images. In that case, normal extraction returns little or nothing, and we need optical character recognition, called OCR.

## 10 — Measure extraction

Page count and character count are useful first checks. They do not prove the text is correct. We still inspect a safe sample or test known facts. The Day 5 script stops when it extracts fewer than fifty non-space characters.

## 11 — Keep the prompt bounded

The document becomes part of the request. A file may exceed the model’s context limit, contain private data, or contain instructions we should not trust. Set size limits, choose approved content, and treat document text as data.

## 12 — Write with intent

Write mode creates a new file or replaces an existing file. Append mode adds to the end. Before using write mode in production, decide whether overwriting is intended. Create the output folder explicitly and record where the result went.

## 13 — The complete failure map

A missing path, unsupported extension, oversized file, wrong encoding, damaged PDF, scanned PDF, provider failure, and write-permission error are different problems. Good software tells the user which layer failed and what to do next.

## 14 — Lab 5.A: customer FAQ

[OPEN `summarize.py`.]

The first lab reads a customer returns-and-shipping FAQ as UTF-8, asks for three useful bullets, and saves the answer as `summary.txt`. Notice that the code builds its input and output paths from the lab folder.

## 15 — Prove text ingestion locally

[SWITCH TO `demo-commands.html` AND RUN THE TEXT PREFLIGHT.]

We read the real sample without calling a provider. We print its name, byte size, character count, and a safe opening line. This proves the file path and decoding work.

## 16 — Lab 5.B: IT handbook

[OPEN `extract_points.py`.]

The second lab reads every page of a two-page IT handbook. It joins the extracted text, checks whether useful text exists, asks for five first-week facts, and saves them as `key_points.txt`.

## 17 — Prove PDF extraction locally

[RUN THE PDF PREFLIGHT.]

We use the same `pypdf` package as the lab. The check prints the page count and extracted character count. If both are sensible, our local extraction path works. This still does not prove every table or visual layout was preserved.

## 18 — Controlled failures

[RUN THE INPUT CLASSIFIER.]

We test supported text, supported PDF, an unsupported spreadsheet name, and a missing path. These failures are intentional. They show that validation can return a clear action before any provider call.

## 19 — Production boundary

In production, allow only required formats, cap file size and page count, scan untrusted uploads, isolate parsers, restrict output paths, and avoid logging private document text. Add OCR only as a separate, measured path with its own quality checks.

## 20 — Completion gate

Day 5 is complete when the sample text and PDF pass local ingestion checks, unsupported input gets a useful message, output behavior is understood, and the evidence sheet records the limits. Live AI summaries remain a separate check when valid credentials are available.

Next, Day 6 combines the foundation skills into the Smart Summarizer project.
