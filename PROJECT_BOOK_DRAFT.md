# Project Book Draft

## Project Title
Property Violation Detection and Salesforce-Based Review Workflow

## Team Context
This project was developed in collaboration with a client working on code-enforcement and property-condition workflows related to Buffalo and West Seneca. The project goal is to support the identification, review, and documentation of visible exterior housing and property violations using street-level imagery, then organize that information in a workflow that can support legal and municipal follow-up.

## Problem Statement
Manual code-enforcement review is slow and difficult to scale. The client needs a way to:
- collect current street-level property imagery
- identify visible exterior violations
- organize those violations by address/parcel
- support human review and verification
- eventually use the results for enforcement, case preparation, and financial/legal prioritization

## Initial Scope
At the beginning of the project, the team was asked to help build a computer-vision-assisted workflow for detecting exterior property/code violations from images. The early meetings focused on:
- properties in and around Buffalo and West Seneca
- identifying houses in disrepair
- working only from public-view imagery
- creating a web-based tagging workflow
- building or improving training data for future model use

## How The Scope Evolved
As meetings progressed, the scope became more concrete and operational:
- the project shifted from a general AI idea into a structured workflow
- Salesforce became the central system of record
- the `parcels` object became the main object for storing property-level information
- user roles were clarified: watchers, inspectors, liaisons, and staff
- the UI goal became a Salesforce-connected image-labeling interface
- the data pipeline expanded to include GoPro video, frame extraction, and geolocation/address assignment

## Stakeholders
- Client / prosecutor / project lead
- Municipal inspectors and liaisons
- Community watchers
- Student development team
- Finance/data-analysis collaborators

## Core Use Case
The system is intended to support a workflow like this:

1. Capture street-level video or images of properties.
2. Extract still images for individual houses/properties.
3. Associate the image with an address and parcel identifier.
4. Store the image in Salesforce using a standard naming convention.
5. Present the image in a UI for human tagging.
6. Save tagging results back to parcel-linked records.
7. Use the resulting information for verification, prioritization, and later legal/enforcement support.

## Main Functional Requirements Gathered From Huddles

### Image/data requirements
- Work only with visible exterior conditions from public view.
- Support images from historical sources and new field capture.
- Use GoPro video as a major input source.
- Extract still frames from video.
- Link frames to the correct property/address.

### UI requirements
- Provide a simple image-tagging interface.
- Support bounding-box tagging on images.
- Show parcel/address names in a human-friendly way.
- Hide backend naming complexity from normal users.
- Eventually support different user behavior by role.

### Salesforce requirements
- Use Salesforce as the central storage/workflow system.
- Tie image records to parcel records.
- Use parcel identifiers / print key / SBL logic in the backend.
- Support unverified vs verified tagging flows.
- Update parcel records and create linked records/cases when images are tagged.

## User Roles

### Watchers
Trusted community users who help identify visible issues.

### Inspectors
Authorized users who can verify actual violations for formal follow-up.

### Municipal liaisons
Stakeholders who review or coordinate issues in a municipal context.

### Staff
Internal users responsible for uploads, management, and broader workflow control.

## Technical Architecture

### Planned high-level flow
GoPro video -> frame extraction -> address/geolocation association -> standardized file naming -> Salesforce storage -> UI-based human tagging -> record updates / review workflow

### Major components

#### 1. Video/image pipeline
- Accept GoPro video input
- Extract still frames
- determine likely corresponding property/address
- improve precision around side-of-street and distance/vehicle movement issues

#### 2. Tagging UI
- Show an image linked to a parcel
- allow bounding-box annotation
- allow violation category selection
- eventually support watcher vs inspector flows

#### 3. Salesforce integration
- store parcel-centered information
- store tagged and untagged images
- use naming conventions to drive logic
- support future notifications, cases, and record updates

## Design Decisions

### Why Salesforce
Salesforce was selected as the main system because the client already uses it for parcel and workflow management. Rather than creating a disconnected tool, the project moved toward integrating the UI and image management into the existing parcel-centered workflow.

### Why naming conventions matter
The team discussed using a standardized file naming convention to encode parcel/address context and workflow state. This helps the system distinguish:
- original images
- unmarked images
- AI-annotated images
- human-tagged images

### Why human labeling still matters
A major insight from the meetings was that labeled data is necessary for both model testing and future training. Even with automation, human review remains central, especially for:
- generating a reliable labeled dataset
- evaluating model quality
- supporting later inspector verification

## Progress By Workstream

### Requirements and workflow understanding
- multiple huddles captured client workflow in detail
- enforcement/legal context was clarified
- image categories and practical violation types were refined

### UI work
- early image-tagging UI prototypes were shown
- later work moved toward Salesforce-connected UI structure
- parcel/image selection logic became more concrete

### Video pipeline work
- frame extraction and geolocation modules were built separately and then connected
- one challenge was assigning the correct house, especially distinguishing left/right side of the road
- later iterations reportedly improved address-matching accuracy substantially

### Data strategy
- the team identified labeled data as a major bottleneck
- the plan shifted toward extracting many stills from video and then labeling them through the UI/community workflow

## Key Challenges

### 1. Labeled dataset shortage
The team did not yet have a sufficiently large labeled dataset for strong evaluation or robust model training.

### 2. Address precision
Early pipeline versions struggled with correctly matching frames to the exact property, especially when:
- houses were close together
- the camera captured the opposite side of the street
- the car stopped or moved slowly

### 3. Integration complexity
The project involved combining:
- video processing
- image storage
- Salesforce logic
- UI design
- future enforcement-oriented record handling

This made the final workflow more complex than a simple standalone model demo.

## Current State At Audit Time
- Requirements are well understood.
- Workflow and architecture are defined.
- UI direction is clear and partially prototyped.
- Video extraction and address-linking pipeline are partially implemented.
- Salesforce-based integration is in progress.
- A larger labeled dataset is still needed.

## What Was Learned
- solving the correct workflow mattered more than only building a model
- human-in-the-loop design is critical
- data quality and labeling strategy are central, not secondary
- existing enterprise systems like Salesforce strongly shape technical decisions

## Remaining Work
- finalize Salesforce-connected labeling UI
- complete image ingestion and naming workflow
- expand labeled data volume
- connect tagging outputs cleanly to parcel-linked records/cases
- strengthen evaluation metrics for the automated pipeline

## Final Deliverables
- UI prototype / Salesforce-connected labeling interface
- documented workflow architecture
- repository with code artifacts
- Trello/task history
- project book
- handoff/sign-off materials for the client

## Suggested Appendix Items
- screenshots of UI
- screenshots of Salesforce parcel object / image records
- sample naming convention
- sample extracted frames from GoPro video
- sample tagged images
- architecture diagram

## Short Conclusion
This project developed from a broad idea about AI-based code-violation detection into a more grounded workflow system that combines computer vision, human labeling, and Salesforce-based case organization. The most important outcome is not just a model, but a practical structure for capturing, reviewing, and organizing property-condition evidence in a form the client can continue building on.
