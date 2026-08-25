# AGENTS.md

Instructions for AI coding agents working in this repository.

## What this project is

The public website for Humans Being Great. Right now it is a single
"coming soon" placeholder page. The real site has not been built yet.

The placeholder is deliberately plain: **no branding, no logo, no real
content.** Do not add a company name, tagline, logo, colours-as-branding,
social links, or contact details unless explicitly asked. It is a
placeholder on purpose.

## Structure

```
index.html    the entire site, self-contained
.gitignore
```

`index.html` holds its own CSS in a `<style>` block. There are no external
files, no images, no fonts to fetch, and no JavaScript. Keep it that way
unless asked otherwise — the whole page is meant to be one file that loads
instantly.

The page uses CSS custom properties (`--bg`, `--fg`, `--muted`, `--line`)
defined at the top, and respects `prefers-color-scheme`. Change colours
there rather than scattering literals through the stylesheet.

## Build

**There is no build step.** No package.json, no bundler, no framework, no
dependencies. Vercel serves `index.html` from the repo root as a static
file.

Do not add build tooling, a static site generator, a framework, or a
`vercel.json` unless explicitly asked. Adding any of these breaks a setup
that currently works with zero configuration.

## Deploying

Push to `main` and Vercel deploys automatically to
<https://humansbeinggreat.vercel.app>, usually within a minute. Pull
requests get their own Vercel preview URL.

There is nothing to run or trigger by hand. Do not add deploy scripts or
CI workflows for deployment — Vercel already handles it.

## Git authentication

This repo authenticates to GitHub over **SSH**
(`git@github.com:humansbeinggreat/humansbeinggreat.git`), using an ed25519
key on the owner's Mac.

An HTTPS personal access token was tried first and failed repeatedly. **Do
not change the remote back to HTTPS, and do not suggest personal access
tokens.** If a push fails, the cause is something else.

Never write credentials, tokens, or keys into any file in this repo.

## Current state

The background is currently mustard (`#e1ad01`). This was a deliberate
test to confirm the push-to-deploy pipeline works end to end — it is not a
design decision. Expect it to be reverted to a neutral background before
any real work begins.

## Working with the repo owner

The owner is not a developer and works in plain language. Explain changes
in plain terms, avoid jargon, and prefer doing the work over handing over
terminal commands to run.
