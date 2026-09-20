# Day 2 — simple read-aloud transcript

## 01. Make model output reliable

Welcome to Day 2. Yesterday we sent a request and read the response. Today we make that response safer for software to use.

We will turn messy customer reviews into structured records. Then we will deliberately send broken data into our validator and prove that it is rejected.

## 02. Today’s finish line

By the end, you can explain structured output, parsing, validation, retry, and fallback in everyday words.

Your evidence is a review sorter with three protection layers: check the response, retry a limited number of times, and return a safe result for human review if every attempt fails.

## 03. The real work problem

One friendly paragraph may be useful to a person. It is difficult for software to count, sort, filter, or route.

A support team with hundreds of reviews needs consistent fields. Each review should have a sentiment, a topic, and a short summary.

## 04. Conversation versus a filled-in form

Chatty text can change shape from one answer to the next. A structured record uses the same labels every time.

That predictable shape lets normal code read one field without guessing where it appears in a paragraph.

## 05. A system instruction is the job description

The system instruction sets the model’s job and rules for the request. We keep it separate from the customer review.

Use five parts: role, task, rules, what to do when unsure, and output format. Each part removes a kind of guesswork.

## 06. The five-part checklist

Role says who the assistant is. Task says what it must do. Rules set boundaries. Unsure tells it not to guess. Format defines the response shape.

Short, precise instructions are enough. We improve them when real output shows a gap.

## 07. JSON is a filled-in form

JSON is text written as labelled values that software can read. Curly braces hold one record. Square brackets hold a list of records.

In our sorter, each record has sentiment, topic, and summary. The labels must match what our code expects.

## 08. Parsing changes text into data

The provider returns text, even when that text contains JSON. Parsing turns the JSON text into a Python list or dictionary.

Our helper also removes common JSON code fences. Parsing can still fail when the text is malformed, so parsing is not the final safety check.

## 09. Shape is not the same as correctness

Valid JSON only proves that the punctuation can be parsed. It does not prove required fields exist or that sentiment uses an approved value.

We need schema validation after parsing. We also need human or business checks when the meaning matters.

## 10. Define the accepted schema

The Pydantic Review model describes valid data. Sentiment can only be positive, negative, neutral, or unclear. Topic and summary must be strings.

If a field is missing or an allowed value is broken, validation raises a clear error before the program trusts the result.

## 11. The reliable pipeline

The order matters: request, parse, validate, and only then use the result.

If parsing or validation fails, retry within a small limit. If every attempt fails, return a safe fallback marked for human review.

## 12. Show the finished result

The happy path prints one clean row per review. The deterministic failure demo then rejects an unsupported sentiment and a missing summary.

We label this output shape as illustrative until the live commands produce observed output.

## 13. Lab 2.1 — request structured output

[OPEN `review_sorter.py`.]

The system instruction names the exact fields and allowed sentiment values. All five reviews are sent together. The response is parsed and printed as a table.

## 14. Run the review sorter

[SWITCH TO THE DEMO COMMAND PAGE. Run the setup gate, then the review sorter.]

If it succeeds, check the number of rows and required fields. If the provider rejects the request, report the real error and continue to the local validation proof.

## 15. Lab 2.2 — validate before use

[OPEN `reliable_sorter.py`.]

The code parses the response and passes it into the Review schema. Returning from the function happens only after validation succeeds.

## 16. Retry is bounded

A retry gives a temporary or variable failure another chance. It is not an endless loop.

Our maximum is three attempts. Each attempt may create cost and delay, so production code also needs timeout, backoff, and rate-limit handling.

## 17. Fallback is an honest safe result

After all attempts fail, the program returns sentiment unclear, topic needs-review, and a summary saying automatic classification failed.

The fallback does not pretend the classification succeeded. It keeps the program running and sends the item toward human review.

## 18. Force broken data safely

We do not wait for the model to fail during a recording. We directly give the validator an unsupported sentiment and a record with a missing field.

This test is deterministic. It proves the schema rejects those known bad examples without making a provider call.

## 19. What this proof does and does not show

Validation proves the output has the declared shape and allowed values. It does not prove the sentiment is factually or semantically correct.

Retries can increase cost and repeat a bad request. Fallback needs an owner, a queue, and monitoring in a real system.

## 20. Day 2 completion gate

Day 2 is complete when the structured sorter works, malformed data is rejected, retry is bounded, fallback is clearly flagged, and your evidence notes record the result and limits.

Next, we will strengthen the Python skills used inside these workflows.
