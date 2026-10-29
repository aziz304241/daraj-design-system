# Daraj Design System — Passwordless Authentication

## Deliverables
- `index.html`: design-system component library showcase.
- `auth-qa.html`: interactive Passwordless Authentication showcase and QA matrix.

## Preview
Once the GitHub Pages workflow completes, the passwordless auth page should be available at:
`https://aziz304241.github.io/daraj-design-system/auth-qa.html`

## Figma
- [Daraj_V1](https://www.figma.com/design/25TliLYP8KXTMYDwnSbeEF/Durj_V1)
- [Passwordless Auth screens and QA](https://www.figma.com/design/25TliLYP8KXTMYDwnSbeEF/Durj_V1?node-id=2549-8047)
- [Reusable auth component variants](https://www.figma.com/design/25TliLYP8KXTMYDwnSbeEF/Durj_V1?node-id=2553-8057)

## Behavior and integration notes
- This is a front-end simulation. It does not send real OTP emails or perform real Google/Apple authentication.
- Validate email syntax in the client for usability and always validate again on the server.
- The server must own OTP issuance, expiration, attempt limits, resend limits, and cooldowns.
- Use a generic response that does not disclose whether an email address already has an account.
- OTP UI should support paste and platform autofill, focus movement, accessible labels, and auto-verification after six digits.
- Disable duplicate submissions while email or social authentication requests are in flight.
- Never treat the demo code in the showcase as a production credential.

## QA checklist
- [ ] Empty email cannot submit.
- [ ] Invalid email has a field-level Arabic error.
- [ ] Network/server errors preserve the entered email and allow retry.
- [ ] Rate limiting displays a server-provided retry time.
- [ ] OTP supports paste/autofill and only accepts six digits.
- [ ] Invalid OTP shows error, clears digits, and returns focus to the first cell.
- [ ] Expired OTP enables resend when allowed by the server.
- [ ] Resend maximum shows a cooldown / blocked state.
- [ ] Google and Apple buttons have default, hover, loading, and disabled states.
- [ ] No passwords, names, or phone number fields are introduced.
