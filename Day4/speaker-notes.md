# Day 4 — simple read-aloud transcript

## 01. APIs, secrets, and failures

Welcome to Day 4. Today we open the boundary between our Python program and an outside service.

We will inspect what we send, what comes back, and what a program should do when the exchange fails.

## 02. Today’s finish line

By the end, you can explain an API request and response, protect an API key, read common status codes, and decide whether to fix, retry, or stop.

Our core proof uses controlled local errors, so it remains repeatable without waiting for an outside service to fail.

## 03. An API is a software counter

An API gives one program a documented way to ask another system for work. Our code follows the API contract without needing the provider’s internal implementation.

The boundary matters because data, credentials, time, cost, and failure cross it.

## 04. Request out, response back

A request contains the destination, authentication, headers, and a body or parameters. For our model call, the body includes instructions, messages, model settings, and output limits.

The response carries a status, content or an error, and useful metadata.

## 05. Headers describe the exchange

Headers carry information about the request or response. Authorization identifies the caller. Content type says how the body is encoded.

Never print or record the authorization value. Logs may include header names and safe metadata, but must redact secrets.

## 06. The API key is both access and billing identity

An API key proves that the request is allowed and connects usage to an account. Anyone with the key may be able to spend that account’s budget.

Keep it in local secret storage, never in code. If it leaks, revoke or rotate it and investigate usage.

## 07. Read the request before sending

Inspect the system instruction, user messages, output limit, and selected configuration. Ask whether the data is authorized and minimized.

Do not print the key. A request review should explain what leaves the machine without revealing authentication.

## 08. Read the response as evidence

The response object contains generated content, provider, model, input tokens, output tokens, and approximate cost in our helper.

These fields help explain behavior and usage. Approximate cost is not a provider invoice.

## 09. Output limits can cut an answer short

`max_tokens` limits how much output the model may produce. A very small limit can stop the response mid-sentence.

Our helper does not expose every provider stop field, so the lab uses output-token count as a warning signal, not perfect proof.

## 10. Status codes categorize the result

Two hundred means the request succeeded. Four hundred errors usually point to the request, authentication, permissions, or rate limit. Five hundred errors point to the outside service.

The number narrows the next action. It does not replace the error message.

## 11. Fix errors and temporary errors are different

A 400, 401, or 403 normally needs a real change. Repeating the same request will probably fail again.

A 429, server error, or connection interruption may be temporary. These may be retried later within a limit.

## 12. Backoff means wait longer between attempts

Retrying immediately can make overload worse. Backoff waits before trying again, often increasing the delay each time and adding a small random difference.

Always set a maximum number of attempts and a timeout.

## 13. Retry only when repeating is safe

Reading data is often safe to repeat. Sending an email, charging a card, or creating an order may cause a duplicate action.

Before retrying a side effect, use an idempotency key or another duplicate-prevention method.

## 14. Use an error taxonomy

Name the failing layer: invalid user input, authentication, permission, rate limit, network, provider, parsing, or programming error.

Different layers need different owners and actions. A clear category makes support and monitoring useful.

## 15. Show the finished error handler

The safe wrapper tries the provider call. If an exception occurs, it converts technical evidence into a short action message and returns normally.

Graceful handling does not mean hiding the error. Keep safe technical detail in logs and give the caller an actionable result.

## 16. Inspect Lab 4.A

[OPEN `read_response.py`.]

Find the request fields before the call and the response fields after it. Run live only when provider access is valid.

## 17. Inspect Lab 4.B

[OPEN `handle_error.py`.]

`friendly_message` maps error evidence to advice. `safe_ask` catches the outside failure and prevents the whole program from crashing.

## 18. Prove every error branch locally

Use small fake exceptions with controlled status codes. Check the returned advice for 400, 401, 403, 429, and 500, then test a connection-style name and an unknown error.

This deterministic test exercises the real translator without a provider call or secret.

## 19. Production boundaries

Do not retry authentication or malformed requests without changing them. Do not retry side effects blindly. Redact keys and unnecessary user data from logs.

Use timeouts, bounded attempts, backoff, idempotency, metrics, alerts, and an owned fallback path.

## 20. Day 4 completion gate

Day 4 is complete when you can describe the request and response, secrets remain private, every controlled error maps to a useful action, and retry decisions include limits and idempotency.

Next, we will work with files and document ingestion.
