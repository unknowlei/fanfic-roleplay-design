# Character-Focused Mode

Use this reference when the user wants recognizable characters from an existing work, with characterization as the main purpose. Keep source-world context to the minimum needed to preserve each character's identity.

Character-focused mode is a peer of canon-restoration mode. Its authored content consists of character portrayals and optional major scenes, without a source-story progression or chapter-stage control system.

## Required Choices

Before drafting, ask the user to choose both:

- Character coverage: major and popular characters, or most characters including supporting characters.
- Whether to create scene entries.

Reuse choices already established in the conversation. Wait for any missing choice rather than selecting a default. Ask for the work and source version when they are not yet clear.

If the source has materially incompatible portrayals, use the user's selected version or ask which characterization baseline to adopt.

## Research and Coverage

Follow the main skill's online research and source-handling workflow.

For major and popular characters, select by narrative prominence and supported public recognition. Do not invent popularity rankings.

For broader coverage, include supporting characters for whom usable source information exists. State meaningful coverage gaps and keep unsupported details unspecified.

Consolidate aliases and translations into stable character identities. Give a short proposed character list and, when scenes are requested, a proposed scene list for confirmation. Proceed directly when the user has already approved that scope and requested completion.

## Character Portrayal

Write character-centered entries with enough concrete detail to support actual portrayal. Use five baseline dimensions:

- Appearance.
- Personality.
- Expression.
- Behavior.
- Relationships.

Treat these as starting points rather than an exhaustive field list. Independently research the original work and add other source-supported content needed to portray each character accurately. Choose the additional dimensions and level of detail according to the work and the individual character, and explain defining canonical characteristics concretely. Leave unsupported details unspecified.

Preserve individuality through specific behavioral tendencies and ways of speaking. Maintain the chosen canonical portrayal while reducing dependence on its original setting; do not replace it with generic personality labels or invented traits.

When integrating into a supplied worldbook, follow the main skill's target-character structure and adaptation-choice rules. User-approved adaptations are authored additions within that agreed scope; preserve source accuracy for the remaining material.

Use background only when it is necessary to understand an important trait, motivation, or relationship. Express that dependency as the shortest useful causal summary, then emphasize how it affects present behavior.

Retain relationships that materially shape the character, describing emotional significance, attitudes, forms of address, and interaction patterns. Keep references to source events proportionate to their value for portrayal.

Organize each character around the selected characterization baseline. Standalone character-mode output consists of ordinary-text character entries and the scene entries the user has chosen to include.

## Optional Scenes

Create scene entries only when the user chooses them.

Select the source work's principal or important locations with sustained value for scenes and interaction. Omit locations that are only passed through in the linear story or appear too briefly or infrequently to serve that purpose.

Give each selected location its own ordinary-text entry, limited to:

- Location and scene overview.
- Environmental features.
- Spatial layout.

Use the amount of detail needed to depict the space clearly.

## Merging into a Supplied Worldbook

Follow the main skill's shared JSON inspection and merge workflow. Determine whether the target actually uses MVU before choosing its variable handling.

Use the existing character entries as the content-structure reference. Obtain the user's adaptation choice before introducing content that conflicts with the source portrayal, and apply it to both prose and initial states.

For an MVU target, give new characters the variables required by the target's comparable characters and extend the existing initialization and update configuration. Read [General MVU integration](mvu-integration.md) before changing that integration. For a target without MVU, use ordinary text and prompt instructions without adding MVU or EJS.

Preserve the target's narrative organization and organize imported characterization around the target's needs. Keep source citations, links, and research notes outside the worldbook.
