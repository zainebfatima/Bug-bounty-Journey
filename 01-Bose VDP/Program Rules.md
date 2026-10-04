Bose VDP — Program Rules

Program Information

- Program: Bose VDP
- Platform: HackerOne
- Program Type: Vulnerability Disclosure Program
- Status: Open
- Scope: Open Scope
- Bounty: No bounty / findings are bounty ineligible
- Scope last updated: September 18, 2026
- Program guidelines last updated: February 10, 2026

Scope Strategy

The program uses Open Scope.

Open Scope means the program may accept valid reports on Bose-owned assets even if an asset is not explicitly listed in the scope table.

Important restriction:

«Open Scope does not mean that every Bose-related or apparently related asset can automatically be tested. The asset must be owned/hosted by the program.»

In-Scope Assets

There are 9 listed assets:

Asset| Type| Coverage| Maximum Severity| Bounty
"bose.xx"| URL| In scope| Critical| Ineligible
"support.bose.xx"| URL| In scope| Critical| Ineligible
".bose.xx"| Wildcard| In scope| Critical| Ineligible
Bose Hardware| Other| In scope| Critical| Ineligible
Bose Source Code| Other| In scope| Critical| Ineligible
Bose Credentials| Other| In scope| Critical| Ineligible
Mcintosh| Other| In scope| Critical| Ineligible
Sonus Faber| Other| In scope| Critical| Ineligible
New Stream| Other| In scope| Critical| Ineligible

«Domain names are recorded exactly as displayed in the HackerOne scope information.»

Out of Scope

No separate assets were listed under the Out of Scope section when reviewed.

This does not mean unrestricted testing. Program rules and HackerOne's core ineligible findings still apply.

Program Guidelines

Detailed Reports

Reports should contain detailed and reproducible steps so that the Bose security team can reproduce the issue.

One Vulnerability Per Report

Normally, submit one vulnerability per report.

Multiple vulnerabilities may be chained when chaining is necessary to demonstrate the impact.

Duplicate Reports

When duplicate reports occur, only the first report received is triaged, provided that it can be fully reproduced.

Account Testing

Only interact with accounts that belong to the researcher or where the account owner has given explicit permission.

Researcher Identification Header

The program's test plan asks researchers to add the following HTTP header to requests:

"X-HackerOne-Research: [H1 username]"

Core Ineligible Findings Reviewed

The following categories should generally not be treated as valid findings unless clear security impact is demonstrated:

- Theoretical vulnerabilities requiring unlikely circumstances
- Issues affecting unsupported or end-of-life browsers/operating systems
- Broken link hijacking
- Tabnabbing
- Content spoofing/text injection without meaningful impact
- Physical-access attacks unless explicitly in scope
- Self-XSS or self-DoS unless they can affect another account
- Clickjacking without sensitive actions
- Logout CSRF
- CORS misconfiguration without demonstrated impact
- Software version/banner disclosure
- Descriptive error messages or headers
- CSV injection
- Open redirects without additional security impact
- Optional security-hardening recommendations
- Many rate-limiting issues

Prohibited / Hazardous Testing

Testing that could affect system availability or users must not be attempted unless explicitly authorized.

Examples include:

- DoS/DDoS
- Excessive traffic or requests
- Testing that could affect system availability
- Social engineering/phishing
- Spamming users, forms, or notifications
- Physical-facility attacks

Testing Principle

Before testing any behavior, determine:

1. Is the asset authorized?
2. Is the activity allowed by the program rules?
3. Is the test safe?
4. Can the behavior demonstrate realistic security impact?
5. Can the result be reproduced and documented?

Current Status

Rules and scope research completed.

Next stage: Target Mapping and safe reconnaissance.
