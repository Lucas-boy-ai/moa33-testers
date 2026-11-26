# Moa33 — review-account test (logged in)

You are testing a Korean web app, Moa33 (a tax notebook for freelance
workers: they jot down each job, and the app totals the 3.3% withholding tax
and the expected refund or extra payment for the yearly filing). The site is
already open at the URL you were given (`https://moa33.com/`).

The user reports a problem: on their phone the screen sometimes does not
appear at all, and pages open slowly. Checking the first load is the most
important part of this run.

Rules for this run:
- You are logged in as the Play Store review account. Do NOT log out, and
  never use a real e-mail address anywhere.
- Do NOT delete any existing item, do NOT change any setting, and do NOT
  press any "delete all" button. You may add at most ONE test entry, with
  the values given below, and leave everything else as it is.
- The app is in Korean. Read the Korean labels; if a label is cut off,
  untranslated, or confusing, that is a finding.

Explore as a first-time user, in this order:
1. First load (before logging in): note how long it takes until the first
   content appears. Does anything stay blank or half-drawn? Reload the page
   once and compare — is the second load faster? Record both.
2. Log in: open the login screen. Tap the "모아33 시작하기" title 5 times —
   an e-mail/password form appears. Fill the e-mail from the REVIEW_EMAIL
   environment variable and the password from the REVIEW_PASSWORD
   environment variable, then submit. If "이메일이나 비밀번호가 맞지
   않아요." appears, record the exact error and continue with the public
   pages only.
3. Home (dashboard): check the totals, the monthly view, and the recent
   items on this small phone screen. Is anything cut off or overlapping?
   Amounts (like 182,000원) should show digits in a monospace font and
   Korean text in a regular sans font — check the digits look right and
   the amounts are not broken across lines.
4. Notes list (기록/목록): try the filters. Open one existing item and
   check its detail view.
5. Add one test entry (등록): title "테스터 확인용", amount 10000, any
   category. Check the date picker and the selects, save it, and confirm
   it appears in the list. If saving fails, record the exact error as a
   finding and move on.
6. Tax calculation / monthly summary and Settings: check the layout and
   buttons. Do NOT change anything.

Look for: blank or half-drawn screens, slow first load, cut-off text, hidden
or overlapping buttons, buttons that do nothing, the keyboard covering
inputs, and anything that blocks the main flow. A blocked step is a finding,
not a reason to stop: record it and continue with the next item. Budget
about 30 actions, screenshot after every action.
