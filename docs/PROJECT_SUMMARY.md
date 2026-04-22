# Project Summary

## Overview

This project explores a workflow for identifying and tagging visible exterior property violations from images. The broader project context involves property-condition review, parcel-based organization, and future integration into a municipal/legal workflow.

## What This Prototype Demonstrates

This prototype focuses on the image-tagging interface layer. It demonstrates:

- loading a property image
- inspecting the image through zoom and pan
- selecting multiple property violation regions in a single image
- assigning a violation label to each region
- editing labels after saving
- exporting structured annotation JSON

## Why This Matters

A single property image can contain multiple visible issues. A tagging interface must therefore support:

- multiple annotations on the same image
- different violation types per region
- easy correction of earlier labels
- structured export for downstream systems

## Intended Future Integration

In the broader system vision, the exported annotation output would later connect to:

- parcel/address records
- backend storage
- human review workflows
- system-generated case or violation records

## Current Limitations

This repository is intentionally lightweight and presentation-ready. It does not yet implement:

- a backend server
- real parcel lookup
- image persistence
- user authentication
- CRM integration

## Demo-Friendly Summary

This repo gives a functional, local, frontend prototype that can be cloned from GitHub, opened in VS Code, and run immediately without additional package installation.
