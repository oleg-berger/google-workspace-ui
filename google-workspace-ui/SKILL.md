---
name: google-workspace-ui
description: Build or refine interfaces explicitly requested in the Google Workspace style of Docs, Drive, Gmail, or Sheets, using Material 3 visual conventions and Tailwind CSS with exact hex colors. Use for Workspace-style UI work, not as a default aesthetic for unrelated projects.
---

# Google Workspace UI

Implement the requested product as a clean, functional workspace familiar to users of Google Docs, Drive, Gmail, and Sheets. Use the requirements below as the project's visual contract. They are a Workspace-inspired implementation profile, not a claim of official Google affiliation or exhaustive Material 3 compliance.

## Scope and precedence

- Preserve the user's application, content, framework, language, and existing functional behavior. Apply these constraints to the requested UI; do not redesign unrelated screens.
- Use Tailwind CSS for implementation. Prefer existing project setup and reusable components; do not replace the framework or install a second styling system solely for this skill.
- Explicit user choices take precedence over generic design advice from other skills. Do not introduce a different visual identity merely to make the result more distinctive.
- Use these visual rules for design mockups as well, while respecting the user's requested artifact format. This skill does not authorize publication, account changes, or modifying an external design file that the user has not requested.

## Workspace layout

- Use a persistent or collapsible left sidebar with a white or softly tinted background. Place a Material icon to the left of each label. Give the active item a pale-blue rounded pill, medium-weight text, and an identifiable selected state.
- Use a flat top app bar: app logo/name at the left, a wide rounded search field in the center, and utility/profile controls on the right. Adapt search and navigation to narrow screens without horizontal overflow.
- When creating an entity is a primary page action, use a prominent create FAB near the upper-left navigation area or bottom-right. Use a plus icon, a rounded square or pill, and a restrained shadow. Do not add a FAB to pages without a meaningful create action.
- Keep working content dominant. Use white surfaces over a soft gray/blue canvas, restrained dividers, and practical table/list density. Do not turn every row into a decorative card.

## Exact palette and Tailwind contract

Use explicit arbitrary-value Tailwind classes for product colors; do not substitute approximate palette utilities such as `bg-blue-500`, `text-gray-600`, or `bg-gray-100`.

| Role | Exact color / class |
| --- | --- |
| Primary action | `bg-[#0B57D0]` or `bg-[#1A73E8]`, with `text-[#FFFFFF]` |
| Canvas | `bg-[#F8F9FA]` or `bg-[#F0F4F9]` |
| Content surface | `bg-[#FFFFFF]` |
| Selected item | `bg-[#E8F0FE] text-[#0B57D0]` |
| Subtle hover | `hover:bg-[rgba(26,115,232,0.08)]` |
| Main text | `text-[#202124]` |
| Secondary text | `text-[#5F6368]` |
| Hairline divider | `border border-[#E0E3E7]` |
| Positive status | `bg-[#E6F4EA] text-[#137333]` |
| Attention status | `bg-[#FEF7E0] text-[#8A4B00]` |

Choose one primary blue and one canvas color for each application, then use them consistently. Keep secondary green, yellow, and deep-blue accents semantic and muted. Do not use random gradients, decorative multicolor washes, heavy black borders, or heavy shadows. Keep the theme light unless the user requests dark mode.

## Typography and spacing

- Prefer Roboto. Use Open Sans or system-ui sans-serif as fallbacks. Google Sans is appropriate for headings only when legitimately available in the environment; do not assume it is installed or fetch proprietary font files.
- Use a consistent hierarchy: body text 14–15px at weight 400, navigation/action labels at 500–600, and clear restrained headings. Use readable line height and allow text to wrap without clipping.
- Use 16px or 24px internal padding for cards and panels, with a coherent spacing scale. Keep related controls together and separate distinct content areas with whitespace.
- Match content width to the task: wide tables and document workspaces may use the available width; paragraphs should remain readable rather than stretching across the entire desktop.

## Components and states

- Cards and dialogs: 16–24px corner radius. Inputs and buttons: 8px or a full pill. Sidebar selections: 16px or a full pill. Use corner geometry consistently by component role.
- Prefer thin `#E0E3E7` borders or borderless surfaces. If elevation is useful, use a diffuse shadow such as `shadow-[0_1px_3px_rgba(0,0,0,0.05)]`.
- Use one icon family throughout: Google Material Symbols or Material Icons, in a consistent Outlined or Rounded variant. Reuse an existing compatible setup; do not mix in Lucide, emoji icons, or unrelated packs. Pair icon-only controls with accessible names and tooltips where useful.
- Keep real controls functional: connect navigation, search, form submission, and state changes within the requested scope. Show meaningful loading, empty, error, disabled, and success states where those actions need them. Do not imply that an external integration works if it is only mocked.
- Preserve visible keyboard focus, sufficient text contrast, and accessible form labels. Use more than color alone for selection and status. Keep dialogs and collapsible navigation keyboard usable.

## Delivery and verification

Inspect the existing interface and its relevant source before editing. Build with real product content and reusable components. When a running preview is available, visually check desktop and narrow layouts for text overlap, clipped labels, inconsistent spacing, and table overflow; repair observed defects before delivery. Run existing checks appropriate to the change.

When the requested deliverable is an inline code implementation, return only the clean, functional HTML/CSS or framework components, with Tailwind styling that follows this contract. Do not add unsolicited design essays. For requested file edits or design artifacts, deliver the edited files or artifact link in the requested format, with only the necessary completion and verification information.
