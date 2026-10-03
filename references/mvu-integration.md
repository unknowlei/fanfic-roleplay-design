# MVU Integration

Use this reference when the active task requires MVU integration. Write generated content and instructions in Simplified Chinese.

Assume Tavern Helper and the applicable MVU/EJS dependencies are installed and ready. Work directly on the worldbook and its configuration. Installation questions, environment checks, and setup assistance are provided only at the user's explicit request.

## Core workflow

1. **Read the applicable tutorials.** Actually read the MVU tutorial, CHANGELOG, and Tavern Helper variable and script documentation before editing. Read the EJS documentation when EJS is involved, and the two StageDog guides when using MVU-Zod. Use the formats established by the supplied files and compatible documentation.

2. **Provide complete support.** Create initialization, current-state injection, update rules, output format, required runtime scripts, and any required structure definitions or registration for standalone new integrations. When merging, extend the corresponding existing initialization, variable-list injection, update rules, output format, and required Schema or registration in place, without creating duplicate MVU entries or a parallel system. Configure necessary output handling and user-requested displays.

3. **Follow the supplied JSON.** Determine whether the target uses MVU before adapting it. For an MVU target, reuse its fields, legal values, initialization, update protocol, and state scope. If existing characters have variables, give each new character corresponding variables using same-kind characters' fields, types, and initial-value conventions; populate character-specific values according to the user's confirmed OOC adaptation choice. Otherwise, for a non-MVU target, merge ordinary text without adding MVU or EJS. Character-focused integration uses the target's character states without constructing the source work's storyline or requiring a stage field.

4. **Keep the integration compatible.** Use the target's documented storage and read APIs and one compatible protocol throughout. Keep affected EJS references synchronized with field changes and preserve unrelated variables. If necessary MVU configuration is external to the supplied JSON, request its companion files before modifying that configuration; do not create parallel initialization or output protocols. MVU maintains state; EJS reads it to select content.

5. **Deliver the required files.** Provide the worldbook and necessary content-specific companion scripts, with a concise description of the configuration changes. Keep research material, source links, and citations outside the generated worldbook.

## Required first-party reading

- [MVU tutorial](https://github.com/MagicalAstrogy/MagVarUpdate/blob/beta/doc/tutorial.md)
- [MVU CHANGELOG](https://github.com/MagicalAstrogy/MagVarUpdate/blob/beta/CHANGELOG.md)
- [Tavern Helper variable types](https://n0vi028.github.io/JS-Slash-Runner-Doc/guide/%E5%8A%9F%E8%83%BD%E8%AF%A6%E6%83%85/%E5%8F%98%E9%87%8F/%E5%8F%98%E9%87%8F%E7%B1%BB%E5%9E%8B.html)
- [Tavern Helper script library](https://n0vi028.github.io/JS-Slash-Runner-Doc/guide/%E5%9F%BA%E6%9C%AC%E7%94%A8%E6%B3%95/%E8%84%9A%E6%9C%AC%E5%BA%93.html)
- [ST-Prompt-Template README](https://github.com/zonde306/ST-Prompt-Template/blob/main/README_CN.md)
- [ST-Prompt-Template API reference](https://github.com/zonde306/ST-Prompt-Template/blob/main/docs/reference_cn.md)
- [StageDog mvu-character-card skill](https://github.com/StageDog/tavern_helper_template/blob/main/.agents/skills/mvu-character-card/SKILL.md)
- [StageDog mvu-variable-framework skill](https://github.com/StageDog/tavern_helper_template/blob/main/.agents/skills/mvu-variable-framework/SKILL.md)
