Day 2 — Target Mapping & Initial Recon

🎯 Goal

Understand the authorized web targets from the Bose VDP scope and begin safe reconnaissance.

📌 What I Learned

1. Understanding the Target Scope

From the HackerOne Burp Suite Project Configuration, I confirmed:

- "bose.xx" is included.
- "support.bose.xx" is included.
- "*.bose.xx" is included for subdomains.
- HTTP port "80" is included.
- HTTPS port "443" is included.
- The path pattern "^/.*" means all paths are included.
- The configuration contains no exclusions.

2. Understanding Wildcards

The "*" in:

"*.bose.xx"

means that subdomains under "bose.xx" can fall within the defined scope.

For example, a hostname such as "api.bose.xx" could match the wildcard rule if it actually exists.

The wildcard does not mean that every possible subdomain exists.

3. Passive Reconnaissance

I learned that passive reconnaissance means collecting information that is already publicly available instead of directly interacting with the target.

The basic idea is:

Discover → Verify → Understand → Document

4. Subdomain Discovery with Subfinder

I installed Subfinder version "2.16.0".

I ran:

"subfinder -d bose.xx"

Result:

0 subdomains found

This does not prove that no subdomains exist. It only means that Subfinder's available sources did not return any subdomains for this run.

5. Certificate Transparency with crt.sh

I searched the exact scope value on crt.sh:

"bose.xx"

Result:

No certificates found

This also does not prove that no certificates or subdomains exist. It means crt.sh had no results for the exact value searched.

6. Understanding httpx

I learned that httpx is used to check whether discovered or known web hosts respond over HTTP/HTTPS.

I installed httpx version "1.12.0".

Because "support.bose.xx" was explicitly listed in the authorized scope, I attempted to verify it with httpx.

Result:

No host result was displayed.

The httpx UI dashboard warning was not an error; the dashboard was simply disabled.

🧠 Important Lessons

- A scope tells me what I am authorized to investigate.
- A wildcard does not mean I should guess random subdomains.
- A tool returning zero results does not necessarily mean nothing exists.
- Different reconnaissance sources can give different results.
- I should verify information instead of assuming it is correct.
- I should not replace an unclear scope value with a guessed domain such as "bose.com".
- Passive reconnaissance is useful for learning about a target while minimizing direct interaction.
- Reconnaissance is not the same as vulnerability testing.

🛠️ Tools Used

- HackerOne
- Burp Suite Project Configuration
- Subfinder "v2.16.0"
- crt.sh
- httpx "v1.12.0"

📊 Results Summary

Method| Result
Scope/Burp configuration| Confirmed web targets and ports
Subfinder| 0 subdomains
crt.sh| No certificates found
httpx| No host result displayed

🚫 Vulnerability Testing

No vulnerability testing was performed today.

The focus was only on understanding the scope, target mapping, passive reconnaissance, and basic host verification.

➡️ Next Step

Continue understanding and mapping the authorized target before moving into any vulnerability testing.

Methodology:

Rules → Scope → Map → Recon → Understand → Observe → Hypothesize → Test → Verify → Document → Report
