# Enumerator Guide: Coffee Farmer Survey (Uganda)

Created by Erick Busuulwa ([devericklasco](https://github.com/devericklasco)).

## Purpose

This interview collects structured data on household coffee farming context, recent shocks, and farmer preferences for AI advisory delivery. Your role is to administer the questionnaire consistently, neutrally, and respectfully.

## Step-by-step administration flow

1. Confirm you are at the correct household and greet the respondent politely.
2. Open the form and complete Interview Setup fields first (`enumerator_id`, location, respondent code).
3. Read the consent script exactly as written. Do not paraphrase key rights.
4. If consent is not given, thank the respondent and complete Visit Outcome only.
5. If consent is given, continue module by module in sequence.
6. Ask questions as written. Use neutral probes only when needed.
7. Capture GPS near the farm entrance when safe and feasible.
8. Complete Visit Outcome and notes before finalizing the form.
9. Review answers for missing required values before submission.

## Consent script

English:
We are collecting information about coffee farming and advisory services. Your participation is voluntary. Your answers are confidential and used only for research and program planning. You may skip any question or stop at any time. Do you agree to continue?

Luganda:
Tukungaanya amawulire ku kulima emmwanyi n’obuweereza bw’amagezi ku bulimi. Okwetaba kwo kwa kyeyagalire. Eby’oddamu bya kyama era bijja kukozesebwa mu kunoonyereza n’okuteekateeka pulogulaamu yokka. Osobola okubuuka ekibuuzo kyonna oba okulekera awo wonna. Okkiriza tugende mu maaso?

## Neutral probing tips

- Use open and neutral prompts: “Please tell me more about that.”
- Do not suggest an answer option.
- If unsure, repeat the question slowly.
- For quantities (land, yield, price), ask for best estimate if records are unavailable.
- Keep tone calm and non-judgmental.

## GPS capture instructions

- Stand at the farm entrance or another safe, open point.
- Wait a few seconds for better satellite lock.
- If possible, capture when accuracy is below 15 meters.
- If GPS fails after reasonable attempts:
  - move to a clearer sky view,
  - retry once,
  - if still failing, continue interview and note the issue in `visit_notes`.

## Common mistakes and how to avoid them

- Skipping consent script: always read it fully before asking `consent_given`.
- Wrong respondent code format: use team-issued format and validate before moving on.
- Entering coffee acreage larger than total land: verify both answers with the respondent.
- Missing “other specify” text: when “other” is selected, fill the follow-up text field.
- Submitting without review: check required questions and outcome fields before final submit.
