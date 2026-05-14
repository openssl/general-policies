# OpenSSL AI Policy

## Overview

OpenSSL welcomes contributions from all developers, including those who use
AI-assisted coding tools. This policy sets out the rules for using such tools
when contributing to OpenSSL.

This policy applies to all public OpenSSL repositories, including all
repositories under [https://github.com/openssl](https://github.com/openssl).

These rules exist to protect OpenSSL's users, its license integrity, and the
legal clarity of its codebase.

---

## The Two Core Requirements

If a **non-trivial portion** of your submission has been created using an
AI tool you must:

1. **Declare it in your commit message** using an `Assisted-by` trailer, and
2. **Have signed a CLA that includes the AI clause.**

Both requirements apply together. Neither alone is sufficient.

---

## 1. Declaring AI Contributions

### What counts as "non-trivial"?

A non-trivial portion of a submission has been created with an AI tool when it
has generated meaningful code, logic, or documentation — not merely assisted
with trivial tasks like autocompletion of a single line, reformatting, or
spell-checking.

If in doubt, declare it as a non-trival contribution.

### How to declare it

Add an `Assisted-by` trailer to your commit message in the format
`Assisted-by: {agent}:{model}`, where `{agent}` is the tool or interface
you used and `{model}` is the specific underlying model. Always include the
model name and version where known, so that the declaration is meaningful:

```
Assisted-by: Claude:claude-sonnet-4-6
Assisted-by: ChatGPT:gpt-4o
Assisted-by: GitHub Copilot:gpt-4.1
```

A commit may have more than one `Assisted-by` trailer if multiple tools
were used.

### Where to put it

[Trailers](https://git-scm.com/docs/gitglossary#Documentation/gitglossary.txt-trailer)
go at the end of the commit message, separated from the body by a blank line:

```
Fix memory leak in EVP_PKEY handling

Rewrite the cleanup path in evp_pkey_free() to correctly release
resources when an error occurs during initialisation.

Assisted-by: Claude:claude-sonnet-4-6
```

---

## 2. The CLA Requirement

OpenSSL has issued a new version of its CLA, which includes an AI clause.
Before submitting any contribution that includes non-trivial AI-generated
content, you must have signed this new CLA.

Signing the old CLA is **not** sufficient for AI-assisted contributions, even
if you have previously signed it. You must sign the new CLA in full — it is
not possible to simply agree to the AI clause in isolation.

The old CLA remains valid for contributions that do not include non-trivial
AI-generated content. If you are not using AI assistance, there is no need to
re-sign.

The new CLA requires that you confirm you have the right to submit the
AI-generated content and that you accept full responsibility for it.

---

## Your Responsibility

**You are responsible for everything you submit, whether or not AI helped
write it.**

This means:

- **Review all AI-generated code** before submitting it. Do not submit
  output you have not read, understood and tested.
- **Ensure correctness.** AI tools can produce plausible-looking but
  incorrect, insecure, or inefficient code. Security is critical to OpenSSL —
  AI-generated code must meet the same standards as any other contribution.
- **Avoid copyright violations.** Do not submit AI-generated code if you have
  reason to believe it reproduces third-party copyrighted material.
- **Check for test coverage.** AI-generated code must be accompanied by
  appropriate tests, just like any other contribution.

The OpenSSL project maintainers may reject or request revision of any
submission, including AI-assisted ones, that does not meet project standards.

---

## What This Policy Does Not Do

This policy does **not** prohibit the use of AI tools. You are free to use
whatever tools help you contribute effectively.

This policy does **not** create a lower bar for AI-assisted contributions.
All code is held to the same quality, legal and security standards regardless of
how it was written.

This policy does **not** permit submissions where no human has reviewed the
content. AI may assist, but a human must direct the work, review the output,
and be accountable for what is submitted.

---

## Summary

| Situation | What you must do |
|---|---|
| AI wrote non-trivial parts of the submission | Add `Assisted-by` trailer; have signed new CLA |
| AI only helped with trivial tasks (e.g. single-line completion, spell-check) | No special action required |
| Unsure whether the contribution is "non-trivial" | Declare it anyway |

---

## Questions

If you are unsure whether your use of AI tools requires declaration, or if you
have questions about the CLA, please ask in the
[OpenSSL GitHub Discussions Q&A forum](https://github.com/openssl/openssl/discussions/categories/q-a)
before submitting.
