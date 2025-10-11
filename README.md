# Qvantel Event Mappings
Prototype Storing the Event Mappings in a different Format

This repository serves as the definitive Source of Truth for all event transformation mappings (JSLT). 
All mapping definitions are stored in human-readable YAML format and are version-controlled via Git.

The old process of using Google Sheets for mapping definitions is now considered a DRAFT ONLY process.

## New Workflow for Mapping Changes

1.  **Create a Branch:** Start a new Git branch for your change (e.g., `feature/11009-update-field-x`).
2.  **Edit `mapping.yaml`:** Modify the YAML file in the relevant event directory (e.g., `11009_UsageEvent/mapping.yaml`).
3.  **Update Fixtures (Optional but Recommended):** Update `source_example.json` and `target_example.json` if the change is significant.
4.  **Open a Pull Request (PR):**
    * **Crucially:** The PR description **must** include the "What" and the "Why" of the change.
    * Require review from the R&D Engineer (for technical validation) and the Product Manager (for business validation).
5.  **Merge:** Upon approval, the change is merged.

## Directory Structure

Each directory represents a unique Event Type (e.g., `[Event ID]_[Event Name]`).
```text
[Event ID]_[Event Name]/
├── mapping.yaml          # The Source of Truth: Source/Target/Transform definition.
├── source_example.json   # A sample of the RAW incoming event.
├── target_example.json   # The expected transformed output for testing.
└── README.md             # Specific notes, custom functions, and links for this event.
```
