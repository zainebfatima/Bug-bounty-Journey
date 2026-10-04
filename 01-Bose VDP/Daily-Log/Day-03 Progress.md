📅 Daily Progress Log

Day: Day 3

Date: 2026-09-30

Target: Bose (VDP) — HackerOne

Today's Goal
Confirm the exact scope domain (".xx" ambiguity from 
Day 2) before proceeding with any active recon.

What We Did
- Reviewed the in-scope assets table again — confirmed 
  "bose.xx", "support.bose.xx", "*.bose.xx" appear 
  consistently, not just in one place
- Attempted to view raw page source via browser DevTools 
  to check for a masked/truncated domain — inconclusive 
  (HackerOne is a JavaScript-rendered app, source didn't 
  reveal hidden text)
- Tried copy-pasting the domain directly from the scope 
  table — confirmed it pastes as literal "bose.xx"
- Checked the "Submit Report" form's Asset dropdown — 
  same ".xx" value shown there too, confirming consistency 
  across the platform
- Reviewed Hacktivity tab for Bose (VDP) — found multiple 
  resolved reports, but titles/details are private, so 
  they didn't help confirm the domain
- Visited bose.com directly (passive, non-testing) and 
  checked for a security.txt file — got a 404
- Searched bose.com's official contact/support page — 
  found no public security email; support only offers 
  chat and call
- Found an AI-assisted summary confirming Bose only 
  accepts vulnerability reports via the HackerOne 
  Submission Form, not direct email
- Found one email — privacyandsecurity@bose.com — listed 
  for privacy/data concerns, not vulnerabilities directly
- Sent a scope clarification email to 
  privacyandsecurity@bose.com asking whether "bose.xx" 
  refers to bose.com or represents multiple regional domains

What We Found
- The scope domain is displayed as "bose.xx" consistently 
  across every part of HackerOne (table, dropdown, and 
  report form) — this is not a display/truncation bug
- Bose's own privacy policy link (referenced inside 
  HackerOne's own report template) uses "bose.com" — 
  suggesting ".xx" may be a placeholder representing 
  multiple regional TLDs (.com, .de, .co.uk, etc.)
- Bose has no public security email — all vulnerability 
  reports must go through HackerOne
- Hacktivity shows real resolved reports (2 on bose.xx, 
  22 on *.bose.xx) — confirming researchers have 
  successfully tested and been paid/credited on this 
  scope, even with the ".xx" format

What We Learned
- When scope is ambiguous, the correct and professional 
  action is to ask the program directly — not guess a 
  "real-looking" domain
- HackerOne's "Open Scope" policy exists partly to handle 
  cases like this — it allows valid reports on Bose-owned 
  assets even if not explicitly/clearly listed
- Passive verification (viewing a site's public pages, 
  footer, security.txt) is safe and doesn't count as 
  "testing" — useful for pre-recon fact-finding
- Private/undisclosed Hacktivity reports still provide 
  useful signal (proof that testing IS happening there) 
  even without revealing technical details

Evidence / References
- Bose (VDP) scope table (HackerOne)
- Bose (VDP) Submit Report form — Asset dropdown
- Bose (VDP) Hacktivity tab
- bose.com/.well-known/security.txt (404)
- bose.com support/contact page
- Email sent to privacyandsecurity@bose.com

What Is Completed?
- [x] Verified ".xx" is consistent across all HackerOne 
      surfaces (not a rendering bug)
- [x] Confirmed Bose has no public vulnerability email
- [x] Sent scope clarification request to Bose

What Is Still Left?
- [ ] Await response from privacyandsecurity@bose.com
- [ ] Decide whether to treat ".xx" as literal scope or 
      wait for confirmation before any active recon
- [ ] Identify a second, clearer VDP target to run in 
      parallel while waiting

Next Day Plan
1. Check for a reply from Bose regarding scope clarification
2. Browse HackerOne Directory for a new VDP target with 
   an unambiguous (.com-format) scope
3. Begin passive recon (subfinder/httpx) on the new target 
   while Bose clarification is pending

Questions / Things to Learn
- Does HackerOne officially use ".xx" or similar 
  placeholders for multi-region companies? (worth 
  researching this pattern generally, not just for Bose)
- What is the typical response time for VDP programs to 
  scope questions?
