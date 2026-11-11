# Changelog: Widgets API Labs

**Date:** 2026-11-09
**Comparison:** Changes from the previous commit on this branch (`25b8fc7`). The skill's script could not compare against `main` because `main` uses nested Create/List/Get folders. See `CHANGELOG-Postman-2026-10-15.md` for the changes from `main`.
**Collection file:** `Widgets API Labs.postman_collection.json`

## Structure

The collection is now organized by API entity instead of by course module.

| Folder | Requests |
| --- | --- |
| Regions | Get Regions in Template File |
| Widget Templates | Create, Get All, Get (Custom), Get, Update, Delete |
| Lab Widget Templates | Create Hello World Template, Create Static Image + Content Template, Create Product Grid Template, Create Product Variant List Template |
| Widgets | Create, Get All, Get (Custom), Get, Update, Delete |
| Placements | Create, Get All, Get (Custom), Get by Template File, Get by Widget, Get, Update, Delete |

## Added Folders

- `Lab Widget Templates` contains the four full widget template examples from the course as POST requests.
- `Widgets` and `Placements` replace the combined `Widgets and Page Builder` folder.

## Removed Folders

- `Schema`: its request moved to `Lab Widget Templates`.
- `GraphQL`: its request was removed. The Product Variant List example is now a single create request.
- `Widgets and Page Builder`: split into `Widgets` and `Placements`.

## Added Requests

- `Create Hello World Template` (Lab Widget Templates): same body as `Create Widget Template` in Widget Templates.
- `Create Product Grid Template` (Lab Widget Templates): new example with an `array` schema setting.
- `Create Product Variant List Template` (Lab Widget Templates): new example combining name, schema, `storefront_api_query`, and template markup in one POST.

## Modified Requests

#### `Create Widget Template (Static Image + Content)` → `Create Static Image + Content Template`
- **Name changed**
- Moved from `Schema` to `Lab Widget Templates`. Body unchanged.

## Removed Requests

- `Update Widget Template (New Version)` (GraphQL): replaced by `Create Product Variant List Template`.

## Unchanged

- All requests in `Regions` and `Widget Templates` are unchanged.
- All widget and placement requests are unchanged apart from moving into the `Widgets` and `Placements` folders.
- Collection variables, auth, and collection-level event scripts are unchanged.

## Related Repository Changes

- The lab code folders (`03_WidgetTemplates`, `04_Schema`, `06_GraphQL`) were removed. The repository now contains only the README and the collection.
- `README.md` now includes setup instructions, per-lab guidance, and resource links.
