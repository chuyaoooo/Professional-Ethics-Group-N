# COMP3041 Coursework Part 1 Proposal

## 1. Selection of Software Application or Platform

### 1.1 Overview of the Selected System

Our group has selected Courtsite (https://www.courtsite.my), a Malaysian web-based reservation and payment platform operated by Courtsite Web Solutions Sdn. Bhd. Functioning as a multi-sided business-to-business-to-consumer (B2B2C) system, Courtsite connects recreational athletes with local sports venues ("Partner Centres") to view, book, and pay for facilities.

Courtsite satisfies all three coursework selection criteria:

- **Hands-On Accessibility:** It is a live, publicly accessible web platform where our group can register accounts, test booking flows, inspect network telemetry via browser developer tools, and audit policies without barriers.
- **Niche Scope:** Unlike global platforms (e.g., Grab or Shopee), Courtsite serves the localised niche of Malaysian sports venue management and has zero existing academic studies on Google Scholar, IEEE Xplore, or ACM Digital Library.
- **Ethically Relevant Features:** The platform raises key ethical concerns by: (1) collecting and sharing personal data across independent venues and third parties; (2) enforcing non-refundable payments while disclaiming liability for venue disputes; and (3) relying on bundled consent and unilateral contract modifications.

---

## 2. Preliminary Investigation

### 2.1 Investigation Methods

We combined four methods. **(1) Documentary analysis** of Courtsite's Terms of Use and Privacy Policy (both updated August 2024), including the Malay-language privacy notice, which we read clause by clause and quoted directly. **(2) Public-content review** of the homepage and the Engineering page, to identify features beyond booking. **(3) An interface walkthrough** of registration, venue search and the booking-to-payment flow. **(4) A written stakeholder enquiry** to Courtsite's legal team on 20 October 2026 (Appendix A; see Section 4.4). Network-traffic and email inspection, a permissions audit and systematic review sampling are planned for Part 2. At this stage our firmest evidence is what the platform's own documents say. How the platform behaves in practice is what Part 2 will test.

### 2.2 Issues Identified

**Issue 1: Bundled consent and data-rights coercion — Linked to feature: account registration and consent notice**

- Privacy Policy cl. 3 lists operational purposes (enabling bookings, processing payments) in the same list as "to directly market and promote our partner centres and our products and services", with no separation. The list is "including but not limited to".
- Cl. 5 calls providing data "optional", but states that failing to consent to the Processing "will" leave Courtsite unable to provide the requested services.
- Cl. 6 applies "the same consequences" to users who limit processing, withdraw consent or request deletion. Terms of Use cl. 9 treats use of the Platform as consent.
- Cl. 1 also lets Courtsite process "any such information as we deem necessary", and assumes, "without independent verification", that users have obtained consent when they supply another person's data.
- *Walkthrough evidence:* [Insert screenshot and observation of the registration form: which fields are mandatory, whether a marketing opt-out exists, and whether consent is a checkbox or implied by use.]

**Issue 2: Asymmetric financial harm through rigid refund rules — Linked to feature: booking confirmation and payment**

- Terms of Use cl. 5: bookings are "confirmed and final"; the user cannot cancel after confirmation and "remain[s] liable to pay the applicable Booking Fees in full". Fees are non-refundable "except in circumstances where there is an occurrence of a technical glitch at no fault of the User". "Technical glitch" is not defined, and changes to bookings depend on each Partner Centre's own policy.
- Cl. 1 and cl. 21 let Courtsite change terms or policies, effective on posting or "without notice", and treat continued use as agreement.
- *Walkthrough evidence:* [Insert screenshot of the pre-payment screen: placement, size and wording of the no-refund notice, and whether the user must actively acknowledge it before paying.]

**Issue 3: Responsibility gap between safety promotion and blanket disclaimers — Linked to feature: intermediary role, safety content, social games and venue lighting hardware**

- Terms of Use cl. 1 describes Courtsite's role as "merely to link the user with Partner Centres". Cl. 11 states the user "shall bear all risk" and has "no recourse to Courtsite". Cl. 13 excludes liability for "loss, damage or injury" and caps claims at amounts paid or due. Cl. 6 sends complaints to be "taken up with each other directly". Cl. 10 requires users to indemnify Courtsite.
- The platform's own features go beyond linking. The homepage promotes safety content ("Play Smart, Stay Ready", "Need help? Call") and social games for users to "make friends". The Engineering page describes "a fleet of Raspberry Pi-powered lighting automation hardware deployed live in venues across Malaysia".
- *Walkthrough evidence:* [Record: where the liability disclaimer appears before booking, if at all; what the safety pages say; what social-game listings show about other players, and whether report/block functions or age checks exist (the Terms require users to be 18+); how the Help Centre describes complaints and incidents compared with cl. 6.]

**Issue 4: Limited transparency in third-party sharing and cross-border transfers — Linked to feature: data disclosure and storage practices**

- Privacy Policy cl. 4 permits disclosure to affiliates, contractors, and marketing, administrative and telecommunications providers, "whether within or outside of Malaysia". Access "may be transferred out of Malaysia" for storage and management. It names no recipients, destination countries or specific safeguards, promising only the "minimum" information Courtsite "deem[s] necessary" and "all reasonable steps" to keep it confidential.
- Cl. 4 opens by saying data will generally not be disclosed without written consent, then lists broad exceptions. Cl. 3 sets retention at "a reasonable period", with no figure. The Engineering page lists AWS among its infrastructure but does not say where user data is stored.
- *Walkthrough evidence:* [Record whether any notice of third-party sharing appears at sign-up or checkout before data is submitted, and how many clicks lead to the Privacy Policy.]

### 2.3 Evidence Status

The clause-level findings above come directly from the live policies. The walkthrough observations marked above, together with unanswered questions on retention, third-party recipients, CCTV and the "technical glitch" exception, are carried into Part 2 as items to verify, not as confirmed failings.

---

## 3. Literature Review

### 3.1 Consent and disclosure of data flows

Courtsite's privacy policy relies on a single, all-or-nothing consent. Solove (2013) argues that this model of "privacy self-management" asks consent to do more than it can, since people cannot weigh costs and benefits when downstream uses are unknown. Obar and Oeldorf-Hirsch (2020) support this empirically: 98% of participants joining a fictitious social network missed clauses sharing their data with the NSA. The two diverge on remedy, however. Obar and Oeldorf-Hirsch favour better consent design, whereas Solove warns that replacing consent with substantive rules restricts individual choice. Closer to Courtsite's category, Guo and Chen (2026) audited 286 sports and health apps and rated 42.3% of their privacy policies "unqualified" against China's data protection law, with cross-border transfer requirements the weakest of the disclosure measures. Even a compliant policy may miss what happens after sign-up: Englehardt, Han and Narayanan (2018) found that about 30% of commercial emails leak the recipient's address to third parties when opened, a flow few users would think to look for. Policies alone are therefore a poor guide to actual data flows, so our investigation also examines Courtsite's emails and network traffic.

### 3.2 Standard terms and choice architecture

Courtsite's no-refund rule sits in terms that few users read. Bakos, Marotta-Wurgler and Trossen (2014) found that only one or two in every 1,000 software shoppers opened the licence agreement, undermining the argument that an "informed minority" of readers keeps standard terms fair. How terms are presented therefore matters. Mathur et al. (2019) found 1,818 dark-pattern instances on about 11% of 11,000 shopping websites, including false urgency and obstacles to cancellation. Luguri and Strahilevitz (2021) show such patterns work: mild ones more than doubled sign-ups to a dubious service without provoking backlash, and less-educated users were more susceptible to them. Where Bakos et al. show that users do not read terms, these studies show that interfaces can exploit that inattention. All three studies are Western markets, so whether similar patterns appear in a Malaysian booking flow is what our walkthrough tests.

### 3.3 Platform responsibility and accountability

Courtsite's terms present it as a neutral link and assign liability to venues and users. Nissenbaum (1996) identified "many hands" and "ownership without liability" among the barriers to accountability in computerised systems. Helberger, Pierson and Poell (2018) build on the many-hands problem, arguing that responsibility should be shared cooperatively between platforms, users and public institutions rather than assigned to one actor. Where Nissenbaum diagnoses how accountability erodes, Helberger et al. prescribe how to redistribute it. Read together, they suggest Courtsite's terms do the opposite, concentrating risk on the parties with least control over the platform's design.

### Synthesis

Across all three themes, formal agreement, whether a consent box or accepted terms, proves a weak guarantee of fairness. This motivates Section 4, where ethical theory supplements the SE Code for decisions that agreement alone cannot justify.

---

## 4. Ethical Framework Proposal

### 4.1 Application of the Software Engineering Code of Ethics

Our ethical evaluation of Courtsite will apply the ACM/IEEE-CS Software Engineering Code of Ethics and Professional Practice (1999), focusing on the professional responsibilities of software engineers towards users, employers and the public.

**Issue 1: Bundled Consent and Data Rights Coercion**

Clause 1.06 requires software engineers to communicate fairly and avoid deception, while Clause 3.12 emphasises respect for user privacy. Courtsite's Privacy Policy combines essential booking functions with secondary purposes, including direct marketing, while warning that restricting data processing may affect service access. These clauses will guide our assessment of whether users are adequately informed and provided with meaningful choices over their personal information.

**Issue 2: Asymmetric Financial Harm via Rigid Refund Policies**

Clause 1.03 requires software engineers to consider whether their products negatively affect users' quality of life, while Clause 3.03 requires attention to ethical and economic consequences. Courtsite's Terms of Use generally prohibit cancellations and refunds after booking confirmation, apart from technical glitches not caused by users. We will evaluate whether this arrangement creates disproportionate financial disadvantages and whether refund restrictions are communicated transparently before payment.

**Issue 3: Responsibility Gap and Platform Accountability**

Clause 1.02 requires balancing organisational and user interests with the public good, while Clause 1.04 emphasises disclosing potential dangers associated with software. Although Courtsite facilitates bookings and payments, its Terms of Use place substantial responsibility for venue-related disputes and injuries on partner centres and users. These clauses provide a basis for evaluating whether the platform's responsibilities are proportionate to its control over relevant software features.

**Issue 4: Third-Party Data Sharing and Cross-Border Data Transfers**

Clause 3.12 requires software engineers to respect individuals' privacy, while Clause 3.13 concerns the ethical collection and authorised use of data. Courtsite's Privacy Policy permits disclosure to external service providers and data transfers outside Malaysia without identifying specific recipients or destination countries. These clauses will guide our investigation into whether the platform provides sufficient transparency regarding data sharing and protection.

### 4.2 Application of Ethical Theories

Two ethical theories will supplement the SE Code: utilitarianism and deontology.

Utilitarianism evaluates actions according to their overall consequences for affected stakeholders. Applied to Courtsite, it allows us to weigh operational efficiency, convenient bookings and business sustainability against potential privacy risks, financial losses and safety concerns experienced by users.

Deontology emphasises moral duties and respect for individual rights regardless of beneficial outcomes. This perspective is particularly relevant to informed consent, personal data protection and transparent contractual conditions. Even where a platform's practices improve efficiency, users should not be treated merely as instruments for commercial benefit.

Together, these theories provide complementary approaches for evaluating consequences and fundamental ethical obligations.

### 4.3 Limitations of the SE Code

The responsibility gap identified in Issue 3 demonstrates a potential limitation of the SE Code. Although the Code establishes professional responsibilities concerning public welfare and software safety, it does not specify how accountability should be distributed among software providers, independent venues and users.

Platform liability arrangements may be determined by management and contractual decisions beyond engineers' direct control. Utilitarianism can help evaluate which stakeholders are best positioned to minimise harm, while deontology considers whether transferring responsibility to users is consistent with fairness and duty of care.

A further limitation arises in differentiating the formal recognition of privacy rights from their practical accessibility. Courtsite's Privacy Policy (2024, Section 6) acknowledges users' rights to request access, correction, restricted processing and deletion, directing enquiries to a general legal email address. Although SE Code Clauses 3.12 and 3.13 establish responsibilities concerning privacy and authorised data use, they do not prescribe a specific mechanism for implementing these rights. From a deontological perspective, respecting user autonomy requires more than acknowledging rights in documentation; users must have a reasonable opportunity to exercise them. This raises an additional question: whether Courtsite's procedures make these rights sufficiently accessible, understandable and effective, without assuming that an email-based process is inherently inadequate.

### 4.4 Stakeholder Engagement and Evidential Limitations

To supplement our analysis of Courtsite's publicly available documentation, an academic enquiry was sent to its legal team on 20 October 2026. The correspondence sought clarification on six matters: mandatory registration data, retention periods, third-party disclosures, personal data rights, CCTV at automated centres and the technical-glitch refund exception (Appendix A). No response had been received as of 2 November 2026.

This introduces an important evidential limitation. Although the policies disclose general practices, several operational details could not be independently established through documentation alone. SE Code Clause 1.06, concerning fairness and accuracy in software-related communications, provides a relevant ethical consideration. However, an unanswered academic enquiry does not demonstrate that Courtsite has failed to fulfil its obligations or that its internal practices are inadequate. Consequently, unresolved matters will be treated as questions requiring verification rather than confirmed ethical failures. This distinction is important for ensuring that the final evaluation remains balanced and evidence-based.

---

## References

Bakos, Y., Marotta-Wurgler, F. and Trossen, D.R. (2014) 'Does anyone read the fine print? Consumer attention to standard-form contracts', *Journal of Legal Studies*, 43(1), pp. 1-35. doi:10.1086/674424.

Englehardt, S., Han, J. and Narayanan, A. (2018) 'I never signed up for this! Privacy implications of email tracking', *Proceedings on Privacy Enhancing Technologies*, 2018(1), pp. 109-126. doi:10.1515/popets-2018-0006.

Guo, R. and Chen, F. (2026) 'Privacy policy compliance of mobile sports and health apps in China: Scale development, data analysis, and prospects for regulatory reform', *JMIR mHealth and uHealth*, 14, e73651. doi:10.2196/73651.

Helberger, N., Pierson, J. and Poell, T. (2018) 'Governing online platforms: From contested to cooperative responsibility', *The Information Society*, 34(1), pp. 1-14. doi:10.1080/01972243.2017.1391913.

Luguri, J. and Strahilevitz, L.J. (2021) 'Shining a light on dark patterns', *Journal of Legal Analysis*, 13(1), pp. 43-109. doi:10.1093/jla/laaa006.

Mathur, A., Acar, G., Friedman, M.J., Lucherini, E., Mayer, J., Chetty, M. and Narayanan, A. (2019) 'Dark patterns at scale: Findings from a crawl of 11K shopping websites', *Proceedings of the ACM on Human-Computer Interaction*, 3(CSCW), Article 81. doi:10.1145/3359183.

Nissenbaum, H. (1996) 'Accountability in a computerised society', *Science and Engineering Ethics*, 2(1), pp. 25-42.

Obar, J.A. and Oeldorf-Hirsch, A. (2020) 'The biggest lie on the internet: Ignoring the privacy policies and terms of service policies of social networking services', *Information, Communication & Society*, 23(1), pp. 128-147.

Solove, D.J. (2013) 'Introduction: Privacy self-management and the consent dilemma', *Harvard Law Review*, 126(7), pp. 1880-1903.

Martin, K. (2019) 'Ethical implications and accountability of algorithms', *Journal of Business Ethics*, 160, pp. 835–850. doi:10.1007/s10551-018-3921-3.

van den Hoven, J. (2008) 'Information technology, privacy, and the protection of personal data', in van den Hoven, J. and Weckert, J. (eds.) *Information Technology and Moral Philosophy*. Cambridge: Cambridge University Press, pp. 301–321.

Mittelstadt, B. (2019) 'Principles alone cannot guarantee ethical AI', *Nature Machine Intelligence*, 1, pp. 501–507. doi:10.1038/s42256-019-0114-4.

---

## Appendix A — Correspondence with Courtsite Legal Team (20 October 2026)

*[Insert screenshot of the email sent to legal@courtsite.my on 20 October 2026, 2:47 PM.]*

The enquiry asked six questions:

1. **Sign-up data:** which details listed in the Privacy Policy are required to create an account, and which are optional.
2. **Retention:** how long account and booking records are kept, and what happens to them after a deletion request.
3. **Sharing and storage:** which categories of third parties receive user data, and in which countries data is stored.
4. **Requests:** how long access, correction or deletion requests normally take, and whether a data protection officer or portability process exists.
5. **CCTV at automated centres:** who operates it, how long footage is kept, and which notice covers it.
6. **Refunds:** what counts as a "technical glitch" under clause 5 of the Terms of Use, and how a user can report one.

Reply requested by 28 October 2026. No response received as of 2 November 2026.
