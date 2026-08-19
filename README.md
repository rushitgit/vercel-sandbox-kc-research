# Vercel Sandbox — CHAIN K git-source security research payload
This repo probes the Vercel Sandbox preparer's git behaviour (submodule recursion, symlink handling, hooks). It is a security research artifact for the Vercel Sandbox HackerOne program. Feel free to look — nothing malicious runs unless a preparer clones with unsafe defaults.

Payloads:
- .gitmodules with submodule URLs pointing at IMDS / internal Vercel services (SSRF probe)
- Symlink escapes at checkout
- Hooks that touch a canary file (opt-in on the preparer's side to run)
