---
name: chair-detector
description: Detect chairs from the camera view.
---

# Instructions

You MUST use the `run_js` tool with the following exact parameters:

- skill_name: `chair-detector`
- script_name: `index.html`
- data: A JSON string with the following optional fields:
  - label: The label to show in the camera view. Use "chair" when the user does not specify one.
  - minScore: Number between 0 and 1. The minimum confidence score for showing a chair detection. Use 0.55 when the user does not specify one.
