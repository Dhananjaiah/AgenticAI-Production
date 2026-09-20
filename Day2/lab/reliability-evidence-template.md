# Day 2 reliability evidence

## Run information

- Date:
- Provider and model shown:
- Review sorter path: `phase-1-foundations/day-02/labs/lab-2.1-review-sorter/solution/review_sorter.py`
- Reliable sorter path: `phase-1-foundations/day-02/labs/lab-2.2-validation-retries-fallback/solution/reliable_sorter.py`

## Output contract

- Required fields: `sentiment`, `topic`, `summary`
- Allowed sentiment values: `positive`, `negative`, `neutral`, `unclear`
- Other rules:

## Happy-path observation

- Number of input reviews:
- Number of valid output records:
- Did every record contain all required fields? Yes / No
- Did every sentiment use an allowed value? Yes / No
- Statements that still need human checking:

## Forced malformed-data test

- Invalid example used:
- Validation error field:
- Validation reason:
- Was invalid data prevented from reaching normal output? Yes / No

## Retry and fallback

- Maximum attempts:
- What triggers a retry?
- What fallback is returned after all attempts fail?
- How is human review signalled?

## Usage and limits

- Calls made:
- Approximate cost shown:
- One successful run proves:
- One successful run does not prove:
- Private or sensitive data deliberately excluded:
