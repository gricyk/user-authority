# user-authority

A Claude Code skill that:

1. **Makes the user's judgment final.** Executes instructions as given: no second-guessing, no unrequested corrections, no silent "improvements". Critical mode only on explicit request ("check me", "critique this").
2. **Hands verification to the user.** No hidden self-review loops. Substantive answers end with a `For your verification:` block listing assumptions, claims to check, and commands or tests to run.
3. **Makes ethics transparent.**
   - `⚠ Model norm:` lines disclose whenever the model's built-in guidelines refuse, soften, omit, add disclaimers or steer.
   - `✝ Decalogue:` checks each request's goal and means against the Ten Commandments (Exodus 20:1–17; Deuteronomy 5:6–21) and offers paths that avoid a conflict.

The skill cannot switch off the model's built-in safety limits. When one applies, the skill reports it openly.

## Install

```bash
git clone git@github.com:gricyk/user-authority.git
cp -R user-authority/user-authority ~/.claude/skills/
```

Start a new Claude Code session. The skill loads as `user-authority`.

## Files

- `user-authority/SKILL.md`: the rules, the response structure, and 6 worked examples
- `user-authority/references/model-norms.md`: a checklist of signs that a model norm is acting, and the disclosure format
- `user-authority/references/decalogue.md`: the scope of each commandment, numbering notes, and the goal/means test
