# Day 1 — simple read-aloud transcript

## 01. Meet the LLM

Welcome to Day 1. Today we will remove some of the mystery around language models.

By the end, you will understand what we send to a model, what it sends back, why tokens matter, and how a clear prompt changes the result. You will also run a repeatable request and record real evidence from it.

[PAUSE. Move to the outcome slide.]

## 02. Today’s finish line

Our finish line has two parts. First, you can explain the main ideas in simple words. Second, you can prove that your code sent a request and received a response.

Your evidence will include the prompt, the observed response, the model reported by the script, token usage, approximate cost, and a short note about limits.

## 03. Start with a real work problem

Imagine a new employee asks for three tips for their first day in an IT job. A model can draft those tips quickly.

But a useful team cannot stop at “the answer looked good.” We need to know what we sent, what came back, what it cost, and which statements still need checking.

## 04. What an LLM is

LLM means large language model. In simple terms, it produces text by predicting likely next pieces of text, one step at a time.

Those pieces are called tokens. This process can produce useful explanations, summaries, and code. It does not turn the model into a database of guaranteed facts.

## 05. Generated text is not guaranteed truth

A sentence can sound natural and confident while still being wrong. When a model invents or misstates information, people often call that a hallucination.

The practical lesson is simple: confidence is not evidence. Important facts still need trusted sources, checks, or human review.

## 06. The request and response boundary

Our program creates a request. The request includes instructions and user content. It may also include model settings.

The provider sends back a response. In our lab, the response object includes generated text, the model name, input tokens, output tokens, and an approximate cost calculated by the course helper.

## 07. Tokens are pieces of text

Models do not process text exactly as people read words. They split text into tokens. A token may be a whole short word or part of a longer word.

We do not need to count tokens by hand. We do need to notice that both the input and output use tokens, because they affect limits and usually affect cost.

## 08. Context is the model’s working space

The context window is the amount of information the model can use in one request. Think of it as a desk with limited space.

Instructions, conversation history, documents, and the current question all need room on that desk. A large context window is useful, but it is not permanent memory and it is not unlimited.

## 09. Prompt anatomy

A useful prompt states the task, gives the needed input, adds clear constraints, and asks for an output format.

For our IT-job example, we name the audience, request exactly three tips, ask for a friendly tone, and require one short sentence per bullet. These details remove guesswork.

## 10. Weak prompt and clear prompt

“Tips for a new job” leaves many choices open. The model must guess the job, audience, number of tips, tone, and format.

The clear version closes those gaps. It will not guarantee perfect text, but it gives us observable conditions that we can check.

## 11. Show the finished result

Before we build, look at the destination. The terminal shows an answer followed by a meter: model, input tokens, output tokens, and approximate cost.

The exact answer and numbers can vary. Our pass condition is the presence of meaningful text and the expected response fields, not one exact sentence.

## 12. Read the request code

[OPEN `first_call.py`.]

The messages list contains one user message. Each message has a role and content. The role says who is speaking. The content holds the text.

Then `chat` sends that list. We keep the full reply because we want the text and the usage information.

## 13. Read the response code

The `reply.text` field contains the generated answer. The other fields show the model and token counts.

The cost value is an estimate from a local price table. It teaches the shape of usage, but it is not an invoice. Prices and supported model names can change.

## 14. Run the first call

[SWITCH TO THE TERMINAL. Use the Day 1 demo page. Run the setup gate, then the first-call script.]

If the command succeeds, read the observed answer and usage fields. Say that this path worked now. If it fails, read the first useful error and identify whether it is local setup, authentication, network, provider, rate limit, or billing.

## 15. Repeatability is not identical wording

Run the same script again. The code and request are repeatable, but the generated wording may change.

That difference matters. Software around a model must check useful properties, such as required format and allowed values, instead of depending on one exact paragraph.

## 16. Compare prompts

[OPEN AND RUN `change_the_prompt.py`.]

Compare the vague prompt with the specific prompt. Look at the number of tips, sentence length, tone, and bullet format.

Then compare the tricky question with and without the careful system instruction. Report what actually happens. Do not pretend the first answer failed if the model correctly rejects the fictional premise.

## 17. A system instruction sets the job and rules

A system instruction is a separate instruction that sets the model’s job or behavior for the request. In this lab, it asks the model to admit uncertainty and avoid invented facts.

This can improve behavior, but it is not a guarantee. High-impact facts still need evidence and validation.

## 18. Record evidence, not impressions

Complete the prompt-notes template. Record the prompt, intended behavior, observed behavior, token usage, the one change you made, and the limits.

Avoid words like “perfect” or “always.” Write what you observed. Never copy an API key, private prompt, or customer data into the notes.

## 19. Troubleshoot one layer at a time

For a missing module, check the active Python path and editable installation. For a missing key, fix the private `.env` file off camera. For authentication, network, rate-limit, or billing errors, use the provider’s error message without exposing credentials.

Change one thing and rerun the same command. That gives us useful evidence.

## 20. Day 1 completion gate

You are done when the repeatable script returns text and usage information, the prompt comparison has been observed, and your prompt notes record the result and limits.

You should now be able to explain an LLM, token, context window, prompt, request, response, and hallucination in everyday words.

Next, we will make model output easier for software to validate and recover when the output is malformed.
