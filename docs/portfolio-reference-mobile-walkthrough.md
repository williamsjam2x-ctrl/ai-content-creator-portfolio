# Portfolio Reference Reverse-Engineering — Mobile Walkthrough (18 October 2026)

## Purpose
This document records the user's supplied 66-second mobile screen recording of https://chrisarts.vercel.app/ as a design and content reference for the user's AI Content Creator / AI Automation portfolio. Learn the presentation logic, not copy another creator's identity, wording, artwork, or claims.

## What the reference demonstrates
### 1. Identity and first screen
- A distinctive portrait/profile image appears at the top.
- A clear professional name is presented as the identity anchor.
- A short role line follows the name (the reference uses designer/developer positioning).
- Three obvious actions are visible: projects, contact, and CV download.
- The first screen quickly tells a visitor who the person is, what they do, and where to go next.

### 2. Page architecture observed in the recording
1. Hero / professional identity
2. About me
3. Vision
4. Skills, represented with compact cards and visual indicators
5. Projects, with preview image, project name, concise explanation, and Demo/Source actions
6. Services, each with an illustration/image, title, description, and contact/view-all actions
7. Contact form
8. Social links and copyright footer
9. Mobile slide-out navigation with section links and GitHub
10. Floating back-to-top control

The site is a long, scrollable single-page portfolio. The mobile menu provides direct section navigation.

## Visual system
- Dark navy background, pale blue/aqua accents, white text.
- Rounded dark cards with visible separation and restrained shadows.
- Strong heading hierarchy and compact sans-serif typography.
- Repeated card patterns make projects and services easy to scan.
- Image previews provide concrete evidence of work rather than relying only on claims.
- Mobile-first layout with a hamburger menu and touch-friendly controls.
- The visual style is more developer/cinematic-dark than the user's previously preferred sky-blue/white scheme. Adopt clarity, structure, proof-of-work and responsive behavior; keep the user's own sky-blue + white + dark-text brand unless a later design decision explicitly changes it.

## Content lessons to adopt
- Put identity and role near the top; do not make recruiters search for the professional name.
- Write a specific role line rather than a vague “creative” label.
- Keep the About section short and grounded in actual experience and goals.
- Describe skills in relation to what the visitor can expect the person to deliver.
- Each project card should show a real preview, clear title, problem or goal, what was built, tools used, and a working case-study/demo link where available.
- Services should state a real deliverable and client value, not generic promises.
- Make contact and CV actions easy to find.
- Use the user's real supplied professional portrait; do not substitute a fabricated AI-looking headshot.
- Avoid inflated skill percentages unless measured and defensible.
- Do not claim a workflow is deployed, production-ready, or client-proven unless verified.

## Reverse-engineered implementation ideas
- Build a responsive single-page layout with semantic sections and stable IDs.
- Use a shared spacing/type scale and reusable project/service card components.
- Add a compact mobile menu that opens, closes, closes after a section link is selected, and remains keyboard-accessible.
- Make every action a real link or working control. CV download must point to the actual CV file; project buttons must not be placeholders.
- Use lazy-loaded, optimized image previews with descriptive alt text.
- Provide visible focus states, sufficient contrast, meaningful link labels, and reduced-motion support.
- Motion/scroll reveals are optional enhancements, not prerequisites; content must remain readable when JavaScript or animation fails.
- Prefer locally controlled assets or stable, properly licensed sources. Pexels may be used for supporting editorial imagery where appropriate, but portfolio work samples must show the user's own work.
- Test on Android-sized screens, including overflow, image cropping, menu state, link destinations, form behavior, and loading without third-party animation libraries.

## Evidence and caveats
- This analysis is based on the supplied mobile screen recording and earlier inspection of candidate source repository https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0.
- The recording visibly shows the reference website in a mobile browser, including hero, About/Vision, Skills, Projects, Services, Contact, and slide-out menu.
- The exact deployed site's source-to-deployment relationship has not been independently proven. Earlier source inspection noted a malformed manifest URL beginning with “htts://”, a potentially empty CV link, hard-coded skill percentages, and menu-handler references that need verification. Treat these as candidate-repository findings, not confirmed defects in every live view.
- Do not copy the reference creator's name, portrait, artwork, text, or brand. Recreate only useful design principles with the user's own identity and verified work.

## Build specification for our portfolio
### Above the fold
- Use the user's real portrait with balanced crop and appropriate size.
- Display the professional name clearly and correctly.
- Use positioning: “AI Content Creator & AI Automation Specialist” (or a concise variant aligned to the actual portfolio scope).
- Add a one-sentence value proposition about creating useful AI-powered content and reliable, tested automations.
- Primary actions: View Projects, Contact Me. Secondary action: Download CV, only when the correct file is present.
- Keep the hero uncluttered and readable on Android.

### Required sections
- About / professional summary
- Core skills and tools (only truthful, demonstrated skills)
- Featured projects / case studies, including workflow diagrams or evidence where relevant
- AI content and video samples
- Automation case study with workflow, validation, error handling, audit trail, human approval, and test results when actually built
- Services / capabilities phrased as deliverables
- CV download
- Contact and professional social links
- Footer

### Project-card evidence pattern
For each featured item, show: (1) problem/context, (2) goal, (3) what was built, (4) tools used, (5) test/evidence, (6) outcome or current status, (7) link to sample/source/demo if available. Clearly label prototypes, in-progress work, and tested builds.

## Pre-deployment QA gate — do not skip
1. Correct name and role; portrait is the user's real photo and is not distorted.
2. Hero looks professional at 360px-wide Android viewport and desktop.
3. All nav links land on the correct section; mobile menu opens/closes reliably.
4. CV button downloads the actual CV; no empty or placeholder links.
5. Every project preview loads; images have useful alt text; no unrelated stock image presented as user's work.
6. Demo/source/contact/social links are checked and open the intended destination.
7. Contact form is functional and tested or clearly not presented as a working form.
8. Text has no spelling errors, unsupported claims, or invented results.
9. Accessibility: contrast, keyboard focus, semantic headings, link labels, reduced motion.
10. Performance: optimized images, no horizontal overflow, no broken assets or console errors where inspectable.
11. Mobile, tablet, and desktop layouts checked.
12. Existing live portfolio remains untouched until the replacement passes QA; deploy as a separate preview first, then obtain approval before switching the live site.

## Final design decision
Use the reference's professional identity hierarchy, strong work previews, meaningful project/service descriptions, clear calls to action, section-based navigation, and polished mobile presentation. Do not blindly clone its dark theme or developer-specific content. Our portfolio must represent the user's own AI content and automation work, use the user's real portrait, retain the agreed sky-blue/white/dark-text identity, and pass the QA gate before deployment.
