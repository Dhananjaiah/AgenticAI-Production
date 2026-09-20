# Day 4 API evidence

## Request inspected

- Endpoint or helper used:
- System instruction:
- User message type:
- Model setting source:
- Maximum output setting:
- Timeout configured:
- Sensitive data deliberately excluded:

## Response inspected

- Provider:
- Model:
- Content present: Yes / No
- Input tokens:
- Output tokens:
- Approximate cost shown:
- Possible cut-off detected: Yes / No

## Error translation test

| Case | Retry? | Expected action | Observed result | Pass? |
|---|---|---|---|---|
| 400 bad request | No | Fix request | | |
| 401 authentication | No | Fix or rotate key | | |
| 403 permission | No | Fix access/model | | |
| 429 rate limit | Later | Back off | | |
| 500 server error | Later | Back off/status page | | |
| connection error | Later | Back off within limit | | |

## Idempotency decision

- Operation being retried:
- Could repeating it create a duplicate side effect?
- Idempotency key or duplicate-prevention method:
- Maximum attempts:
- Timeout:
- Fallback or escalation:

## Limits

- Local simulation proves:
- Live call proves:
- Neither proves:
