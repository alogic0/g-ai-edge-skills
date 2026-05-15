---
name: object-detector
description: Detect selected objects from the camera view, including chairs, people, pets, furniture, vehicles, and other COCO object categories.
---

# Instructions

This skill uses the device camera inside the webview. Do NOT ask the user to upload or provide an image. When the user asks to run object detection, detect objects, find objects, or open the object detector, call `run_js` immediately.

You MUST use the `run_js` tool with the following exact parameters:

- skill_name: `object-detector`
- script_name: `index.html`
- data: A JSON string with the following optional fields:
  - targets: Array of object labels to detect, such as `["chair", "couch", "person"]`. Use an empty array when the user does not specify targets.
  - target: String. A single object label to detect when the user asks for one object.
  - label: String. Backward-compatible single object label; treat it like `target`.
  - minScore: Number between 0 and 1. The minimum confidence score for showing detections. Use 0.55 when the user does not specify one.

The webview includes a target selector, so the user can choose or clear the object list after the camera view opens. It also includes voice controls that announce detections, such as "human detected" for `person`, with robotic voice mode enabled by default.
After calling the tool, tell the user to tap the preview card and allow camera permission.
