---
name: fanfic-roleplay-design
description: 同人角色扮演设计skill：创建或修改 SillyTavern 同人世界书，先选择还原模式或人物模式。支持原作世界与主线还原、人物刻画、可选场景，以及按已有世界书 JSON 的人物结构、MVU 使用情况和变量格式融合新角色。涉及偏离原作的适配时先让用户选择，按需配置 MVU/EJS。
---

# 同人角色扮演设计skill

Build source-grounded canon-restoration or character-focused worldbooks, and integrate fanwork into existing worldbooks. Write user-facing discussion and deliverables in Simplified Chinese unless the user requests another language. Keep the selected adaptation, content scope, and character identities consistent throughout.

- Design or ask about the user's in-world identity, role, background, or introduction into the story only when explicitly requested. When merging, leave existing user-identity and introduction content unchanged unless the user requests changes to it.
- When MVU is used, assume Tavern Helper and the applicable MVU/EJS dependencies are already installed and ready. Proceed with worldbook content and configuration; ask about installation or provide environment setup help only when the user explicitly requests it.

## Mode Selection

Start by selecting exactly one of two peer modes. Reuse an explicit choice already supplied; otherwise ask the user to choose and wait for the answer.

| Mode | Purpose | Required reference |
| --- | --- | --- |
| Canon restoration | Reconstruct the world, narrative style, main story, characters, and important locations. | [Canon-restoration mode](references/canon-mode.md) |
| Character-focused | Prioritize character portrayal and optionally include selected major scenes. | [Character-focused mode](references/character-mode.md) |

Read only the selected mode's reference, then use the shared procedures below. Each mode defines its own questions, content, and organization. Main-story stage control belongs exclusively to canon restoration when MVU is enabled.

## Intake and Decisions

Extract choices already supplied in the conversation. Confirm the work, source version, and whether the user wants a standalone worldbook or integration into an existing JSON. Ask the additional scope questions required by the selected mode.

Distinguish standalone creation from integration into a supplied worldbook. For integration, first read the target JSON and determine whether it already uses MVU. Follow that result: adapt MVU only for an MVU target; otherwise merge through ordinary text without introducing MVU or EJS.

Standalone runtime choices follow the selected mode's reference. Integration in either mode inherits the target JSON's MVU usage.

Before creating or modifying MVU content, read [General MVU integration](references/mvu-integration.md), then actually consult the applicable tutorials linked there. This guide covers runtime support and variable adaptation. Canon restoration additionally loads its stage-control reference when MVU is enabled.

## Research and Coverage

Search the internet for the chosen work before composing its lore. Prioritize the selected original work and official material; use well-maintained secondary references to fill coverage gaps. Distinguish adaptations and resolve conflicting accounts against the selected continuity.

Build a working character inventory for the selected mode and coverage. Canon restoration follows the covered main story and its referenced cast; character-focused mode follows the user's selected character scope. Normalize aliases and translations under stable identities. Allocate detail according to available source material while preserving the agreed coverage. Represent uncertain or unavailable information conservatively.

Keep reference material, source links, provenance, and citation markers exclusively in working notes outside the worldbook, including its entry metadata. Use paraphrase and synthesis. If essential sources are unavailable, explain the specific coverage limit and request material or a scope decision.

## Integration into an Existing Worldbook

Apply this workflow when the user requests integration into a supplied JSON, in either canon-restoration or character-focused mode.

### Read the Target

Read the complete JSON and identify entry structure, IDs, keys, activation settings, insertion positions, priorities, and extensions. Inspect variable paths, types, initial values, allowed values, state storage and reading, update instructions, output protocol, EJS conditions, and script references.

Read the existing character entries to identify their common content organization, required character fields, initial settings, and level of detail. For MVU targets, also identify how comparable characters are represented in the variable structure.

Determine whether the target actually uses MVU from its initialization, state handling, update configuration, and related references. A mention of MVU or the presence of unrelated variables alone is insufficient. If the evidence is ambiguous, ask for the missing information before selecting the integration route.

- **MVU target:** Read its variable format and follow the MVU adaptation workflow.
- **Non-MVU target:** Merge ordinary text entries following the selected mode's content rules. Do not add MVU variables, MVU support components, or EJS.

For an MVU target, use the supplied variable structure and configuration as the integration basis. If an existing component that must be edited is external, request that component's content or file. Consult the technical tutorials before designing MVU changes.

### Match Character Structure and Confirm Adaptation

Write imported characters in a content structure comparable to the target's existing character entries. Include the applicable character sections, required fields, and initial settings used by the target, populated for the new characters rather than copied from another character.

If the target's character structure or world rules require additions or changes that may conflict with the source portrayal, briefly describe the affected aspects and ask the user to choose:

- Allow adaptation to the target's character structure and world rules, including agreed departures from the original portrayal.
- Preserve the original portrayal and fit the target's structure only where the content remains compatible.

Reuse an explicit choice already provided. Wait for the decision before authoring conflicting traits or initial states. Apply permission only within the agreed adaptation scope. If preserving the original portrayal leaves a required target field unresolved, ask how to reconcile that field rather than inventing a conflicting value.

Record the agreed adaptation scope separately from source research so that authored additions are not presented as original-work facts. Use this decision consistently in both character prose and associated variables.

### Adapt the Variables

Apply this section only when the target JSON uses MVU.

Use the target's actual variable format and runtime. Reuse fields with matching semantics, and add or modify fields when required by the user's requested behavior. Preserve unrelated variables and their meanings.

When existing comparable characters have MVU variables, give imported characters the corresponding fields under the target's existing character-variable structure. Follow its types, initial-value conventions, and update behavior, using the user's confirmed adaptation choice for character-specific content.

Follow the selected mode's requirements when mapping its content to target variables. If field meanings or requested behavior conflict, clarify the intended mapping with the user before changing those meanings.

Extend or modify the existing initialization, schema and registration, current-state injection, update rules, output-format configuration, and EJS references as needed. Keep existing protocols when their semantics remain sufficient. Integration must update the target's established MVU components rather than create a second initialization entry, output-format entry, or parallel variable system. If required components are supplied externally, request those companions before changing them.

Replace the behavior the user wants changed directly while preserving unrelated target behavior.

### Merge the Content

In either mode, use the target's character-entry structure and the confirmed original-portrayal or adaptation choice when writing imported characters.

- Canon-restoration integration adds the agreed world foundations, narrative style, main story, characters, and important locations. For an MVU target, character and special-location EJS uses the adapted main-story field; within-stage character changes remain sparse prompt conditions. For a non-MVU target, stage changes and disclosure conditions use ordinary prompt text.
- Character-focused integration adds character portrayals, the minimal background needed to understand them, and major-location entries only if the user chose to create scenes. Adapt dynamic characterization to the target's MVU variables only when it uses MVU; otherwise use ordinary text according to the user's requested behavior. Follow the character-mode reference for scope and portrayal.

Preserve untouched entries, their IDs, unknown fields, and existing activation settings. Give new entries collision-free IDs. Resolve material identity or setting conflicts with the user before combining overlapping content.

Deliver a complete merged JSON containing the preserved and integrated content. Save to a new file by default and retain the supplied original. Include required content-specific companion scripts and a concise explanation of variable changes. Keep research references outside the worldbook.

## Authoring and Delivery

1. Resolve the work, mode, scope, and standalone or integration intent. In character-focused mode, obtain the character-coverage and scene choices. For standalone canon restoration, obtain the MVU choice; for integration in either mode, first determine MVU usage from the target JSON. Research the agreed continuity.
2. Present the selected mode's compact content outline and coverage. For integration, identify the target character structure and obtain the adaptation choice when required; for MVU targets, include the corresponding new-character variables and intended mapping. Obtain confirmation before bulk authoring unless the user has already approved the scope and requested completion.
3. Compose the selected mode's content. Canon restoration uses flexible main-story prose and explicit stage boundaries; character-focused mode prioritizes portrayal and only the user's selected scenes.
4. Apply the selected mode's content and integration rules. If using MVU, consult the required tutorials. Provide complete support for standalone creation; for integration, extend the target's existing MVU components and character variables before merging.
5. Package the finished standalone or merged SillyTavern worldbook JSON and required companion artifacts. For planning requests, deliver the requested level of detail.

Before constructing the export, consult the target installation's export format or current SillyTavern source/documentation for field names and behavior. Use descriptive entry titles, distinctive character and location names and aliases for retrieval, and deliberate activation settings. First match relevant entries, then apply their content-selection rules.

Reference material, source links, provenance, and citation markers belong only in external working notes. Any guidance the model must obey belongs in rendered content or an active instruction entry.

Deliver the worldbook file with a concise description of coverage, the selected control method, and content-specific configuration changes. When prompt-based stage conditions are used, explain that they rely on model interpretation. Report actual completion and limitations without implying an import or runtime execution occurred. Run import, runtime, or other validation only when the user explicitly requests it.

## Primary Technical References

- [SillyTavern World Info](https://docs.sillytavern.app/usage/core-concepts/worldinfo/)
- [SillyTavern source](https://github.com/SillyTavern/SillyTavern)
- MVU, Tavern Helper, MVU-Zod, and EJS tutorials are mandatory reading where applicable, as routed by [General MVU integration](references/mvu-integration.md).
