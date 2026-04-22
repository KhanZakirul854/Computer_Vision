# Audit Packet

## What To Prepare In The Next 2 Hours

### 1. Trello
- Make sure every card has:
  - a clear title
  - owner
  - status
  - evidence link
  - short note on what was completed
- Use these lists:
  - `Backlog`
  - `In Progress`
  - `Blocked`
  - `Done`
  - `For Audit Demo`

### 2. Code Repo
- Push the latest code, even if incomplete.
- Add a `README` that explains:
  - project goal
  - team roles
  - current architecture
  - what works now
  - what is partially working
  - what is not finished
- If there are multiple prototypes, keep them and label them clearly instead of hiding them.

### 3. Project Book
- Include:
  - problem statement
  - client and stakeholder context
  - requirements gathered from meetings
  - design evolution
  - architecture/workflow
  - UI work
  - pipeline work
  - datasets and labeling plan
  - current blockers
  - next steps
- Use the draft in [PROJECT_BOOK_DRAFT.md](/Users/khanzakirul/Documents/Codex/2026-04-22-hey-ai-so-i-will-give/PROJECT_BOOK_DRAFT.md).

### 4. Audit Talking Points
- Be honest about what is complete versus what is prototype-level.
- Show continuity from huddle notes to implementation.
- Emphasize that the system has three connected parts:
  - video/image extraction
  - Salesforce-based UI for labeling/review
  - downstream automation for enforcement support

## What You Can Say In The Audit

### One-paragraph summary
Our project focuses on identifying visible exterior property violations from street-level imagery and integrating that into a Salesforce-centered workflow for labeling, review, and later legal/enforcement use. Across the semester, the project evolved from initial computer-vision ideas into a practical pipeline: extracting frames from GoPro video, linking frames to property addresses, storing them in Salesforce, and creating a UI for human tagging and later inspector verification.

### Current state
- We clarified the client workflow through repeated huddles.
- We identified core user roles: watchers, inspectors, municipal liaisons, and staff.
- We defined the Salesforce `parcels` object as the central record.
- We established naming-convention-driven image logic.
- We built UI concepts for image tagging.
- We worked on extracting still images and geolocating them from GoPro video.
- We identified labeled data generation as the key bottleneck for improving model evaluation/training.

### If they ask “what is done?”
- Requirements gathering is done at a strong level.
- Workflow and architecture are substantially defined.
- UI direction is defined and partially implemented/prototyped.
- Video-to-image/address pipeline is partially implemented.
- Salesforce integration direction is defined.
- Full production-ready integration is not complete yet.

### If they ask “what remains?”
- finalizing the labeling UI inside or against Salesforce
- stabilizing image ingestion from GoPro video
- improving address association accuracy
- creating a larger labeled dataset
- connecting human labeling output cleanly back into Salesforce records/cases

## Suggested Trello Cards

### Done
- `Collected client requirements from huddles`
- `Defined user roles and workflow`
- `Defined parcel-centered Salesforce architecture`
- `Outlined naming convention for images`
- `Created initial image-tagging UI prototype`
- `Tested video frame extraction workflow`
- `Improved geolocation/address-matching logic`

### In Progress
- `Connect extracted frames to Salesforce records`
- `Integrate UI with Salesforce parcel/image data`
- `Generate labeled dataset from extracted frames`
- `Support watcher/inspector tagging flow`

### Blocked
- `Need final client-approved Salesforce field mapping`
- `Need larger labeled dataset for robust evaluation`
- `Need stable hosting/runtime path for full pipeline`

### For Audit Demo
- `Show UI prototype`
- `Show workflow diagram`
- `Show sample extracted frames from video`
- `Show naming convention and parcel linkage logic`
- `Show project book draft`

## Suggested Repo Structure

If your repo is messy, organize it like this:

```text
project-root/
  README.md
  docs/
    audit-summary.md
    project-book.md
    workflow.md
    client-notes.md
  ui/
  pipeline/
  sample-data/
  screenshots/
```

## Demo Flow For Wednesday

1. Start with the problem:
   - exterior code violations are hard to process manually at scale
2. Show the client context:
   - Buffalo / West Seneca
   - legal and enforcement workflow
3. Show the technical flow:
   - GoPro video -> frame extraction -> address association -> Salesforce -> human labeling
4. Show the UI:
   - parcel/image selection
   - bounding-box tagging
5. Show current limitations:
   - training data volume
   - address precision
   - integration not fully finished
6. End with next-step clarity:
   - complete integration
   - expand labeled dataset
   - prepare handoff/sign-off artifacts

## Immediate Priority Order

1. Get your repo and Trello cleaned up.
2. Put the draft project book into your actual submission format.
3. Send the client handoff/sign-off message today.
4. Prepare 3-5 screenshots or clips for the audit.
5. Rehearse a 2-minute explanation of what your team specifically built.
