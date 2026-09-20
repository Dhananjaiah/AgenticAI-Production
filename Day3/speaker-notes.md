# Day 3 — simple read-aloud transcript

## 01. Just-enough Python

Welcome to Day 3. Today we name and practise the Python that has already appeared in our AI labs.

We will keep one real workflow in view: classify customer reviews and decide what action to take.

## 02. Today’s finish line

By the end, you can read variables, functions, lists, loops, dictionaries, and conditions without guessing.

You will prove it by testing the decision function locally, processing a batch, and changing one rule in one place.

## 03. Read code as a story

A useful program can read almost like instructions: load the reviews, classify each review, choose an action, keep the result, and print the summary.

Small functions hide details while clear names show the main story.

## 04. Variables are labelled boxes

A variable gives a value a useful name. The equals sign assigns a value to that name.

Text values are strings and use quotes. Clear names such as `review`, `result`, and `action` explain their purpose.

## 05. F-strings build useful text

An f-string lets us place a value inside text with curly braces. We use it to build prompts and readable output.

The value is inserted when the line runs. Never place an untrusted value into a command and execute it as code.

## 06. Functions are named recipes

A function wraps steps under one name. Parameters are its inputs, and `return` sends a result back.

The function should do one clear job. A good name tells the reader what that job is.

## 07. Type hints explain the contract

In `classify(review: str) -> dict`, the hint says the function expects text and returns a dictionary.

Type hints improve reading and tool support. Python does not automatically validate every hint at runtime, so important boundaries still need real checks.

## 08. Dictionaries store labelled values

A dictionary is a group of labelled values. Our classified result has labels such as sentiment, topic, and summary.

Code reads a value using its key. A missing key raises an error, so validated input matters.

## 09. Lists hold many items in order

A list holds several values under one name. Square brackets create the list, and positions start at zero.

We can ask for its length and append new results to the end.

## 10. Loops repeat one clear process

A `for` loop takes each item from a list and runs the indented block once.

The same code can handle three reviews or three hundred, although outside calls still need limits, cost control, and error handling.

## 11. Conditions choose a path

An `if` statement asks a yes-or-no question. `elif` checks another case, and `else` handles everything left.

Double equals compares values. A single equals sign assigns a value.

## 12. Combine the pieces

For each review, call the classify function, pass the result to the action function, append the result, and print it.

Each line has one purpose. The detailed provider call stays inside `classify`.

## 13. Show the finished workflow

The finished script prints the sentiment, topic, summary, and action for each review.

A negative result goes to support. An unclear result goes to human review. Other results are marked okay.

## 14. Inspect Lab 3.A

[OPEN `sorter_functions.py`.]

Find the function inputs, return values, list, loop, and condition. Read `main` from top to bottom before opening function details.

## 15. Test decisions without a model

The action function only needs a dictionary. We can test positive, negative, and unclear inputs without a network call or API key.

This is a small unit test: one focused piece receives controlled input and returns observable output.

## 16. Run the live sorter

[USE THE DEMO PAGE. Run the live script only when provider authentication works.]

If it succeeds, check three results and three actions. If it fails externally, report the provider error and keep the local Python evidence separate.

## 17. Inspect Lab 3.B

The questions list contains one blank item on purpose. `enumerate` gives a number and question on each pass.

The condition detects blank text. `continue` skips the rest of that pass, preventing an unnecessary model call.

## 18. Force one safe error and fix it

Use a learner copy to create a simple NameError or indentation problem. Read the error type, file, line, and message.

Fix only the named cause, then rerun the same command. Never experiment by changing the private environment file on camera.

## 19. Production boundaries

A loop around a provider call can multiply latency and cost. Add input limits, timeouts, failure handling, and concurrency control before using large batches.

Type hints and clean functions improve code, but they do not replace validation, tests, authorization, or monitoring.

## 20. Day 3 completion gate

Day 3 is complete when you can explain the code, local decision tests pass, the batch skips invalid input, and one routing rule can change without rewriting the workflow.

Next, we will look more closely at APIs, secrets, and failures.
