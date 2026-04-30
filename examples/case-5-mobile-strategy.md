# Case 5 — Mobile Strategy

**Question:** "I'm building a SaaS product for SMBs. Should I build a mobile app?"

*Type: Technical / Strategic Decision. Specific context provided. Strong pull toward "it depends" balance.*

---

## Without Just Do More

> **Most likely: don't build the app. At least not now.**
>
> The practical reasons:
>
> **SMB workflows happen at desks, not on phones.** Core business operations — reporting, data management, configuration — are most naturally done on a computer. Mobile is typically "check something," not "do the work."
>
> **The real cost of an app is underestimated:**
> - iOS + Android (or a cross-platform stack with its own learning curve)
> - App Store review cycles that interrupt your iteration speed
> - Version fragmentation across user devices
> - Support costs roughly double when you add mobile
>
> For an early-stage SaaS, these costs consistently drain resources away from the core product.
>
> **The one situation where you should build:**
> Your product has specific features with a strong mobile use case: approval workflows (a manager needs to sign off while traveling), attendance/check-in, field sales logging, notification and alert delivery.
>
> **Recommended path:**
> 1. Make your web product responsive — usable in a mobile browser for the 1-2 most critical flows
> 2. Observe what users actually try to do on mobile
> 3. When you have specific, clear, high-frequency mobile demand — build for it
>
> Don't let "the competition has an app" drive this. Ask first: what do your users actually need to do on a phone?

---

## With Just Do More

> **Direct answer: probably not, at least not now.**
>
> But the reason isn't just "apps are expensive." There's a more important trap to name first:
>
> **An app is an amplifier, not an exploration tool.**
>
> Mobile works as a force multiplier for teams that have already found product-market fit, have a stable core product, and have identified specific high-frequency mobile use cases. For teams still iterating on their core product, building an app is spending resources to make an unfinished product look more complete.
>
> ---
>
> ## The signals that make mobile the right call
>
> Don't ask "would mobile be nice to have." Ask whether any of these are true:
>
> | Signal | What it means |
> |---|---|
> | Users need to complete a **full operational loop** on mobile — not just view data | Approvals, field logging, inventory scanning, shift check-in |
> | Your **churn analysis** shows mobile experience as a retention issue | Data-driven, not assumed |
> | Your sales team reports that **competitor apps are affecting win/loss rates** | Frontline signal, not speculation |
> | Your core product is **stable and no longer needs major changes** | App is an amplifier — don't amplify an unfinished product |
>
> If none of these are true, building a mobile app is buying the appearance of completeness.
>
> ---
>
> ## Practical alternatives that cost a fraction of native app development
>
> - **Responsive web** — Make your 1-2 most critical flows work in a mobile browser. Near-zero cost, covers most "I need to quickly check something" cases.
> - **Progressive Web App (PWA)** — Installable from the browser, can work offline, supports push notifications. Covers a substantial portion of mobile use cases without app store friction.
> - **Push notifications via email or SMS** — Most "I need mobile" requests are actually "I need to be notified quickly." That doesn't require an app.
>
> ---
>
> ## The only question that cuts through all of this
>
> **What specific thing would a specific user do on their phone, in a specific situation, where their phone is clearly better than a laptop?**
>
> If you can name it concretely — a field sales rep logging a customer visit immediately after leaving the meeting, a floor manager approving a shift swap in real time — build for it.
>
> If the answer is "check dashboards" or "stay updated" — responsive web and notifications handle that. No app needed.

---

## What Changed

**Excellence Bar** pushed past the standard cost-benefit analysis frame. A mediocre answer lists the costs of building an app and suggests checking whether users need mobile. An excellent answer for an *early-stage SaaS product* gives a specific mental model: apps are amplifiers, not exploration tools. That reframe changes how you evaluate the decision entirely.

**Blind Spot** caught two things the baseline missed:
1. The "false balance" trap — the baseline hedged more than necessary, when the situation (early SaaS, SMBs) actually has a fairly clear answer
2. The Progressive Web App alternative — a middle path that the binary "app vs. no app" framing doesn't surface

The phrase "an app is an amplifier, not an exploration tool" only emerges when Excellence Bar demands: *what is the one insight that, if the user understood it, would change how they approach this decision?* The baseline gave a list of factors to weigh. The skill gave a principle to apply.

**The baseline answered correctly. The skill answered usefully.**
