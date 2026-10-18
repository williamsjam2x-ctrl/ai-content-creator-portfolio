# Reference Portfolio Source-Code Analysis — ChrisArts Portfolio 2.0

**Purpose:** Record the source-code analysis of the ChrisArts portfolio as a design and implementation reference for this portfolio. This is an analysis/reference document, not copied source code. The existing portfolio site is to remain untouched while improvements are built and tested separately.

## Reference links

- Live site supplied for investigation: https://chrisarts.vercel.app/
- Strongest source-code candidate: https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0
- HTML: https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0/blob/main/index.html
- CSS: https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0/blob/main/style.css
- JavaScript: https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0/blob/main/main.js
- Web app manifest: https://github.com/Eche-de-Coder/ChrisArts-portfolio-2.0/blob/main/manifest.json

**Verification note:** The repository manifest contains the string `htts://chrisarts.vercel.app/index.html`, which is a typo and a strong clue linking the repository to the supplied domain. The exact live deployment was not conclusively verified against deployed files. Treat this as the best-supported candidate, not a guaranteed exact match.

## 1. Technology and file structure

- `index.html`: page structure, content sections, buttons, navigation and project cards.
- `style.css`: colours, layout, typography, responsive styling and visual transitions.
- `main.js`: particles background, rotating typing effect, mobile side menu, reveal-on-scroll animation and animated skill bars.
- `manifest.json`: installable web-app metadata and theme settings.
- Assets include a profile image, skill icons, project images and video demonstrations.

The implementation is primarily plain HTML, CSS and JavaScript. It uses the Poppins Google Font, Material Symbols, Font Awesome and Particles.js from external CDNs.

## 2. Visual design observations

- Main background: `#1E293B` (dark blue-grey).
- Side menu background: `#0F172A` (deep navy).
- About cards: `#0d1b2a`.
- Hero heading uses powder blue; much of the text is white.
- Circular profile image, rounded content cards and high-contrast buttons.
- Poppins typography.
- A full-screen hero area and fixed hamburger navigation.
- Subtle movement through particles and scroll-reveal effects.

## 3. Interaction and behaviour

- Hero text cycles through messages using a type-and-delete effect.
- Particles.js draws a moving background; pointer interaction repels particles and clicks add particles.
- Hamburger button opens a slide-out side menu with an overlay.
- IntersectionObserver reveals selected sections as the visitor scrolls.
- Skill bars animate to percentages defined in HTML data attributes.
- Navigation links point to About, Skills, Projects, Services and Contact sections.

## 4. Quality issues observed in the candidate source

These observations refer to the inspected repository files; they have not all been confirmed on the live deployment.

1. The Download CV anchor in the inspected HTML has an empty `href`; it needs a real CV destination to work.
2. `manifest.json` contains `htts://chrisarts.vercel.app/index.html`; `htts` is an invalid scheme and should be corrected in any derivative implementation.
3. JavaScript selects an element with ID `closeMenu`, but the inspected HTML excerpt does not show that element.
4. The menu close handler attaches a click listener to `openMenu`, but that function was not defined in the inspected JavaScript excerpt. Test and remove or correct dead code.
5. Skill-bar percentages are hard-coded display values; they should not be presented as independently verified measurements.
6. External fonts and libraries are loaded from CDNs. Check performance and graceful behaviour if a dependency fails.
7. Keyboard accessibility, focus management, reduced-motion preferences, image alt text, mobile layout and all button destinations should be tested before deployment.

## 5. Application to our portfolio

Use the underlying ideas, not a blind copy of another creator's identity or assets.

Our portfolio direction remains **sky blue + white + dark text**, with clean spacing and a professional, human-written feel. Build improvements separately and preserve the existing deployed portfolio as a backup.

Recommended sections:
1. Hero/introduction with a clear AI Automation Expert and Consultant positioning.
2. Short About section.
3. Demonstrable skills and tools.
4. Project cards and evidence.
5. Case studies describing the problem, workflow, validation, error handling, human approval and verified result.
6. Creative work section for Stick Man and AI Filmmaking Laboratory, plus WildMIND Stories where useful.
7. Contact details and working GitHub/project links.
8. Working CV button linked to the correct CV file.

Use real screenshots and approved project media. Pexels can be used for suitable supporting footage or imagery after checking the relevant licence and recording attribution/asset details where needed. Do not use another person's profile photo, personal branding or project assets as if they were ours.

## 6. Required test checklist before deployment

- [ ] Mobile layout checked on Android-sized screens.
- [ ] Navigation opens and closes; links go to the correct sections.
- [ ] Every project/demo/source link works.
- [ ] CV button opens or downloads the correct CV.
- [ ] Contact links work.
- [ ] Images and video load correctly; no broken asset paths.
- [ ] Spelling, contrast, keyboard access and reduced-motion behaviour checked.
- [ ] Project claims match available evidence; no invented metrics or claims of full deployment.
- [ ] Final deployed site checked before sharing with employers.

## Conclusion

ChrisArts Portfolio 2.0 is a useful reference for a compact personal portfolio made with HTML, CSS and JavaScript. Its strongest lessons are the clear section structure, prominent introduction, mobile side navigation and visible project evidence. Our implementation should improve reliability and accessibility while retaining our own visual identity and verified project claims.
