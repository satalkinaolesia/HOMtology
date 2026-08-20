# HOMtology — Codex Repository Instructions

These instructions apply to all Codex tasks in this repository unless the user explicitly overrides them in the current task.

## 1. Project purpose

HOMtology is a landing-page project for an independent residential functionality standard and research/pilot workflow. Preserve the project's current meaning, positioning, and structure unless the user explicitly asks for a strategic or content change.

## 2. Working method

- Work only inside the existing HOMtology repository.
- Start from the repository state provided by Codex for the selected task.
- Do not configure or modify Git remotes.
- Do not use `git push`.
- Do not use GitHub CLI (`gh`).
- Do not request, create, store, or use `GH_TOKEN`, `GITHUB_TOKEN`, personal access tokens, or other GitHub credentials.
- Do not attempt to create a pull request from inside the shell or via `make_pr` if that tool is unavailable.
- Make the requested changes, test them, and commit them locally on the current Codex work branch when appropriate.
- At the end of the task, clearly state that the changes are ready for the Codex interface button **Create PR**.
- Do not make unrelated changes.
- If the request is ambiguous and a wrong assumption could materially affect content, structure, forms, data collection, or branding, ask before making that change.

## 3. Source of truth

- Treat the existing repository files as the source of truth for implementation details.
- Preserve existing working behavior unless the user explicitly asks to change it.
- Before editing a page, inspect the relevant HTML, CSS, and JavaScript rather than assuming how it works.
- Reuse existing design tokens, spacing rules, typography, components, and patterns where possible.
- Avoid unnecessary rewrites of entire files when a focused change is sufficient.

## 4. Design and UX

- Preserve HOMtology's visual identity unless the user explicitly requests a redesign.
- When implementing a reference design, adapt the design principles and interaction patterns rather than copying proprietary text, assets, or branding verbatim.
- Maintain a professional, modern, research-oriented visual tone.
- Keep layouts clean, readable, and visually consistent across sections.
- Prefer purposeful animation over decorative motion.
- Animations should be smooth, lightweight, and should not interfere with reading, navigation, forms, or accessibility.
- Respect `prefers-reduced-motion` for non-essential animations.
- Avoid animation libraries unless they clearly improve the result; prefer CSS and lightweight JavaScript for simple effects.
- If adding a dependency or animation library, explain why it is needed.

## 5. Responsive behavior

- Every visual change must work on desktop, tablet, and mobile.
- Do not treat desktop as the only target.
- Check for overflow, clipped text, broken navigation, oversized headings, awkward spacing, and inaccessible controls on narrow screens.
- Preserve usable tap targets and spacing on mobile.
- Avoid fixed dimensions when fluid or responsive sizing is more appropriate.

## 6. Accessibility

- Use semantic HTML where practical.
- Preserve or improve keyboard navigation.
- Keep visible focus states.
- Use meaningful alt text for informative images; use empty alt text for purely decorative images.
- Maintain sufficient contrast for text and controls.
- Associate form labels with their inputs.
- Do not remove accessibility behavior unless explicitly requested.

## 7. Content rules

- Do not rewrite HOMtology's core messaging, claims, research language, pilot conditions, legal wording, privacy wording, or calls to action unless the user explicitly asks for a content change.
- Preserve the intended distinction between research participation and pilot participation.
- Do not invent statistics, certifications, legal status, partnerships, endorsements, research results, or product capabilities.
- If text appears to be intentionally multilingual, preserve the current language strategy unless instructed otherwise.
- Keep terminology consistent across the site.

## 8. Forms and integrations

- Treat existing form embeds, Tally links/embeds, branching logic, data-collection flows, and external integrations as sensitive behavior.
- Do not replace, remove, rename, or restructure form integrations unless explicitly requested.
- When changing layout around an embedded form, verify that the embed still loads and remains usable on mobile.
- Do not add new tracking, analytics, cookies, or third-party scripts without explicit permission.

## 9. Privacy, legal, and trust

- Do not weaken privacy, consent, terms, or disclosure language.
- Do not add legal claims or compliance statements without explicit instruction.
- Do not expose email addresses, API keys, secrets, tokens, private endpoints, or hidden configuration values in source files, logs, commits, comments, or prompts.
- Never commit `.env` secrets or credentials.

## 10. Images and assets

- Reuse existing repository assets when appropriate.
- Store new site images in a clear repository location such as `assets/images/` unless the existing structure indicates another convention.
- Use descriptive filenames.
- Optimize image dimensions and file size for web delivery.
- Preserve aspect ratio and avoid unnecessary quality loss.
- Add appropriate `alt` text when the image communicates information.
- Do not fabricate external image licenses or ownership claims.
- If an image must be generated outside Codex, leave the code ready for the final asset path and clearly identify the expected filename and dimensions.

## 11. JavaScript and performance

- Prefer the smallest implementation that satisfies the request.
- Avoid unnecessary frameworks or dependencies for a simple static landing page.
- Keep JavaScript scoped and avoid polluting the global namespace where practical.
- Do not break existing event handlers or embeds.
- Avoid large base64 assets inside HTML/CSS when a normal asset file is more maintainable.
- Minimize layout shifts and avoid blocking page load with non-essential scripts.

## 12. Testing before completion

For every task, perform the checks that are relevant to the change. At minimum:

- verify the changed files are syntactically valid;
- inspect the final diff for unintended edits;
- check that links and anchors touched by the task still point to valid targets;
- check for obvious desktop and mobile regressions;
- check that forms or embeds touched by the task still render correctly;
- check that no secrets or credentials were added;
- keep the working tree clean after the final local commit when a commit is part of the task.

If a proper browser preview or automated test is unavailable, say so explicitly instead of claiming visual verification that was not performed.

## 13. Completion format

At the end of each task, give a concise summary containing:

1. what was changed;
2. which files were changed;
3. what checks were performed;
4. any limitation or item that still needs visual/manual verification;
5. the statement: **Ready for Create PR in the Codex interface.**

Do not ask the user for GitHub credentials and do not attempt shell-based pushing.
