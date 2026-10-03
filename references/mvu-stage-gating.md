# Canon-Restoration MVU Stage Gating

Load only when canon-restoration mode is selected and MVU is enabled. First read [MVU integration](mvu-integration.md).

- Use one main-story stage field; its default path for a new integration is `story.stage`.
- For an existing MVU JSON, adapt a suitable existing main-story field and its legal values instead of forcing a new path.
- Derive stage values, their order, the initial value, and transition conditions from the selected main storyline; keep ordering and mappings as static data.
- The value identifies the chapter actually entered. Update it when the narrative enters a new chapter, not merely when that chapter is mentioned.
- MVU initializes, saves, and updates the field through the target's supported message-state mechanism.
- EJS only reads this field and static stage data to select character and special-location content; it does not modify state.
- Emit character material for its corresponding stage or stage range, accumulating applicable revelations while selecting the appropriate current-state version.
- Emit partial special-location information before its designated stage, full information upon entering that stage, and retain the full information in subsequent stages.
- Keep all these EJS conditions tied to the same main-story field without adding character-stage, event, or location-visit variables.
