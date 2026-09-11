# Character Sheet and Prompt Retry

## What will change
- Add an always-available character sheet field where the user can paste or edit their own character definitions before generation.
- Keep automatic character-sheet creation when the field is empty; use the user's sheet unchanged when supplied.
- Add a copy control beside the character sheet with clear copied feedback.
- Add a separate **Retry prompt** control to every panel. It will request a fresh prompt for only that timestamp, save it, and then redraw that panel using the new prompt.
- Keep the existing **Retry** control unchanged: it will continue redrawing from the current prompt.
- Show each panel's current prompt so users can confirm what changed.

## Character consistency
- Strengthen the generated sheet to lock permanent identity traits: gender, age, face shape, skin tone, hair, eyes, build, distinguishing marks, and exact clothing colours.
- Strengthen final image instructions so all matching character traits are repeated without truncating the identity lock too aggressively.
- Ensure prompt regeneration uses the current manual or generated character sheet and preserves the panel's original timestamp and script line.

## Technical details
- Keep all API-key handling server-side and unchanged.
- Extend existing browser state and saved progress rather than adding new storage or services.
- Give image retry and prompt retry separate busy states to prevent duplicate requests.
- Verify type safety, the preview build, and the controls on the current mobile-sized view.
