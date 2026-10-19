# Google Workspace UI

**Make your interface feel right at home next to Google Drive, Docs, and Gmail.**

You know that feeling when you open a Google app and immediately know where everything is? The quiet colors, rounded search bar, clear navigation, and room to breathe.

That’s what this skill helps your AI coding agent build.

No elaborate prompting every time. No guessing which shade of blue looks close enough. Just a consistent set of design rules for clean, practical interfaces inspired by Google Workspace and Material Design 3.

## What it does

The skill guides your agent through the details that make the style work:

- **Familiar layouts.** A useful sidebar, a flat app bar, and a prominent search field.
- **Precise colors.** Actual hex values instead of approximate Tailwind defaults.
- **Clear typography.** Readable text, sensible hierarchy, and consistent spacing.
- **Soft components.** Rounded buttons, subtle dividers, and restrained elevation.
- **Consistent icons.** Material Symbols or Material Icons throughout the interface.
- **Responsive behavior.** Layouts that still make sense when the screen gets smaller.
- **Usable interactions.** Focus states, form labels, feedback, and accessible contrast.

The goal is a workspace people can comfortably use every day.

## A small detail that matters

Instead of this:

```html
<button class="bg-blue-500 text-white">
  Create document
</button>
```

The skill asks for this:

```html
<button
  class="rounded-full bg-[#0B57D0] px-6 py-3 text-sm font-medium text-[#FFFFFF]
         hover:bg-[#0842A0] focus-visible:outline focus-visible:outline-2
         focus-visible:outline-offset-2 focus-visible:outline-[#0B57D0]"
>
  Create document
</button>
```

Small choices add up. A consistent interface comes from getting them right together.

## Install

Place the skill folder in your agent’s skills directory.

For Codex:

```text
~/.codex/skills/google-workspace-ui/
└── SKILL.md
```

On Windows:

```text
C:\Users\<your-user>\.codex\skills\google-workspace-ui\
```

## Use it

Invoke the skill and describe what you want to build:

```text
$google-workspace-ui

Build a student dashboard with a course sidebar, upcoming assignments,
a search bar, and a calendar panel.
```

It also works for refining an existing interface:

```text
$google-workspace-ui

Restyle this dashboard to feel like Google Workspace.
Keep the current content, framework, and functionality.
```

Want dark mode? Ask for it explicitly:

```text
$google-workspace-ui

Add a dark theme with tonal surfaces, pastel accents,
and readable text contrast.
```

The skill keeps the theme light by default.

## The palette

A few of the core light-theme colors:

| Purpose | Color |
| --- | --- |
| Primary action | `#0B57D0` |
| Canvas | `#F0F4F9` |
| Content surface | `#FFFFFF` |
| Selected item | `#E8F0FE` |
| Main text | `#202124` |
| Secondary text | `#5F6368` |
| Divider | `#E0E3E7` |

Tailwind classes use these values directly, such as `bg-[#F0F4F9]` and `text-[#202124]`.

## Fits your project

Already have a framework, working navigation, and real content? Keep them.

The skill is designed to improve the interface within your existing project. It doesn’t require replacing your stack or adding a second styling system. Your explicit design decisions take priority.

It works especially well for dashboards, learning platforms, document tools, admin panels, and other apps where getting things done matters.

## A note on the name

This is an independent skill inspired by Google Workspace and Material Design 3. It is not affiliated with or endorsed by Google, and it is not an official Google component library.

---

**Less time describing rounded corners. More time building something useful.**
