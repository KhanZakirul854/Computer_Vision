# Property Image Tagger Prototype

This is a lightweight standalone audit/demo UI for image tagging.

## What it does
- upload a property image
- enter a parcel/address name
- choose a user role: `Watcher` or `Inspector`
- choose a violation type
- draw bounding boxes on the image
- delete tags
- export annotation JSON

## What it does not do yet
- no Salesforce connection
- no authentication
- no parcel dropdown from a real backend
- no automatic case creation

## Demo suggestion
1. Click `Load Demo Image`
2. Enter a parcel/address
3. Select a violation type
4. Draw 2-3 bounding boxes
5. Click `Export JSON`
6. The UI interaction layer that would later connect to Salesforce parcel/image records
