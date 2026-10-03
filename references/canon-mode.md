# Canon-Restoration Mode

Use this reference when the user selects canon-restoration mode. Follow the main skill's shared research, integration, and delivery workflow.

## Scope and Preparation

- Confirm the work, source version or adaptation, story coverage, cutoff point, and inclusion of supplementary canon. Reuse choices already established in the conversation.
- For a new standalone worldbook, ask whether to use MVU and wait for an explicit choice before designing its variable support.
- For integration into supplied worldbook JSON, inherit the target's detected MVU usage. An MVU target uses its existing variable conventions; a non-MVU target receives plain-text content and prompt conditions without introducing MVU or EJS.
- Research the selected continuity online and build a character roster covering the agreed main story and characters mentioned within that scope. Normalize aliases and translated names.
- Organize the main story into its natural chapters or phases. Use meaningful narrative boundaries to support character changes and special-location information.
- Keep sources, links, citations, and research notes outside every worldbook field, including entry metadata.

## Worldbook Content

### 1. World Foundation

Write one to three entries according to the work's complexity. Cover the setting, social context, major factions, and essential world or power-system rules.

Put detailed character and location descriptions in their own entries.

### 2. Atmosphere and Narrative Style

Write one separate entry defining atmosphere, emotional tone, narrative voice, pacing, dialogue style, and descriptive emphasis.

Translate the work's distinctive narrative qualities into practical writing guidance.

### 3. Main Story

Research the main storyline online and summarize it freely using the work's natural chapter structure. Preserve chronology, important causal connections, central conflicts, turning points, and the involvement of major and supporting characters.

Let the work determine entry count, length, and prose organization. Use stage identifiers to associate character and special-location content with the relevant portions of the story; do not impose a fixed event-by-event template.

Identify the story summary as narrative reference rather than evidence that its events have already occurred in the current conversation.

### 4. Character Portrayal and Stage Changes

Combine stable characterization and changing information in each character's profile. Split entries only when retrieval or length requires it.

Use appearance, personality, expression, behavior, and relationships as the basic descriptive dimensions. Treat these as a starting point rather than an exhaustive field list. Actively research the source material and add whatever other established details are necessary to portray that particular character accurately.

Choose additional dimensions and depth according to the work and the character. Explain distinctive canon traits concretely and leave unsupported information unspecified.

For integration, follow the main skill's target-character structure and adaptation-choice rules. Match the target's required character content and initial settings, and obtain the user's choice before introducing departures from the source portrayal. Keep approved adaptations within their agreed scope.

Organize changing character information by the main storyline's stages. State each section's applicable stage and the point at which its information becomes available or its changes take effect.

With MVU:

- Maintain the main-story stage through MVU and use EJS to open or switch character content based on that stage.
- Use the same main-story stage mapping for every character.
- Describe changes occurring at different points within one stage through brief prompt conditions placed with the relevant character content.
- Keep these conditions sparse and limited to changes that materially affect portrayal. Entering a chapter makes its content available; an event-dependent change applies only after that event actually occurs.

Without MVU:

- Explain all character-stage changes directly through prompts in the character entries.
- State applicable main-story stages and the conditions for changes within each stage.
- Base applicability on events actually established in the conversation. A mention, prediction, or recollection does not itself complete an event in the current scene.

Retain revealed history and identity information where it remains relevant. Use the applicable stage's version of current goals, loyalties, abilities, and relationships. Distinguish narrator-accessible facts from what each character knows.

### 5. Important Locations

Write separate worldbook entries for important locations and classify them by how they are used in the story.

For common locations used frequently, provide plain-text descriptions of the scene, position, environmental features, and spatial layout. Do not use EJS for these entries.

For special locations encountered through story progression, prepare the limited information available beforehand and the full description available upon entering the corresponding chapter. Both levels focus on the scene, position, environmental features, and spatial layout.

- With MVU, use EJS and the shared main-story stage variable to provide the limited description before the chapter and the full description from that chapter onward.
- Without MVU, explain the same chapter-based information conditions through prompts.

## MVU Support and Chapter Gating

Apply this section only when canon-restoration mode uses MVU.

Read [MVU Integration](mvu-integration.md) for general MVU support and required tutorial reading. Read [MVU Main-Story Stage Gating](mvu-stage-gating.md) for the stage variable and EJS content selection. Consult the applicable linked tutorials before creating or modifying MVU integration.

For standalone creation, provide the complete support required by the selected implementation: variable initialization, current-state injection, update rules, update output format, runtime support, and EJS integration. Include schema definitions and registration when the chosen implementation requires them. Configure additional presentation features according to the user's request.

For integration, extend the target's existing MVU components and give imported characters the corresponding variables used for comparable characters. Modify existing initialization and update configuration instead of adding a parallel set of MVU support entries.

Derive stage values, order, initial state, and transitions from the agreed storyline and starting stage. In an existing MVU worldbook, adapt this mapping to the target's variable structure and runtime.

When the user changes variable requirements, update all affected initialization, structure, state injection, update instructions, and EJS references together. Follow the shared integration workflow when the target's existing stages require a scope or meaning decision.
