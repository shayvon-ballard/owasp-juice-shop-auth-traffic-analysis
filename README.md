# owasp-juice-shop-auth-traffic-analysis
# Authentication Traffic Analysis (OWASP Juice Shop)

## Summary
This project documents a passive review of authentication-related network traffic in OWASP Juice Shop using browser developer tools and Burp Suite Community Edition. The goal was to practice identifying login endpoints, validating request/response behavior, and reviewing headers/payload structure safely (non-intrusive).

## Scope
- Passive traffic inspection only (no exploitation)
- Focus: authentication/login request and related traffic
- Tools: Browser DevTools, Burp Suite Community Edition

## Methodology (High Level)
1. Observed baseline application traffic during normal browsing.
2. Identified authentication-related requests (login endpoint).
3. Captured requests/responses in Burp HTTP history.
4. Reviewed request headers + payload structure (credentials redacted).
5. Reviewed response behavior (HTTP status codes and headers).

## Key Observations
- Authentication attempts produced a **401 Unauthorized** response when invalid credentials were submitted.
- No sensitive information was observed in server responses during failed authentication attempts.
- Standard security-related headers were present; no obvious information leakage was identified from passive inspection.

## Evidence
Screenshots are provided in `/screenshots`:
- Figure 1: Initial traffic during normal interaction
- Figure 2: Authentication-related request identified in HTTP history
- Figure 3: Login POST request headers/payload structure (redacted)

## Report
Full report is available here:
- `/report/Authentication_Traffic_Analysis_OWASP_Juice_Shop.pdf`

## Notes on Redaction
All credential values and any potentially sensitive tokens/cookies were redacted prior to publishing.
