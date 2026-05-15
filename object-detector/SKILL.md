---
name: object-detector
description: Detect selected objects from the camera view, including chairs, people, pets, furniture, vehicles, and other COCO object categories.
---

# Instructions

You MUST use the `run_js` tool with the following exact parameters:

- skill_name: `object-detector`
- script_name: `index.html`
- data: A JSON string with the following optional fields:
  - targets: Array of object labels to detect, such as `["chair", "couch", "person"]`. Use `["chair"]` when the user does not specify targets.
  - target: String. A single object label to detect when the user asks for one object.
  - label: String. Backward-compatible single object label; treat it like `target`.
  - minScore: Number between 0 and 1. The minimum confidence score for showing detections. Use 0.55 when the user does not specify one.
