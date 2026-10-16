# Changelog: Widgets API Labs

**Date:** 2026-10-15
**Comparison:** Changes from main branch
**Collection file:** `Widgets API Labs.postman_collection.json`

## Structure

The collection was reorganized from one folder per API resource (Widget Templates, Widgets, Placements, Regions) into one folder per course module. Requests are named `Verb Noun`, with no nested Create/List/Get/Update/Delete subfolders.

| Folder | Course module | Requests |
| --- | --- | --- |
| Regions | Module 2 | Get Regions in Template File |
| Widget Templates | Module 3 | Create, Get All, Get (Custom), Get, Update, Delete |
| Schema | Module 4 | Create Widget Template (Static Image + Content) |
| Widgets and Page Builder | Module 5 | Widgets: Create, Get All, Get (Custom), Get, Update, Delete. Placements: Create, Get All, Get (Custom), Get by Template File, Get by Widget, Get, Update, Delete |
| GraphQL | Module 6 | Update Widget Template (New Version) |

## Added Requests

- `Create Widget Template (Static Image + Content)` (Schema) — body from `04_Schema/02_LabTemplateStaticContent/widget.json`, which now matches the example in the Schema lab
- `Update Widget Template (New Version)` (GraphQL) — body from `06_GraphQL/02_LabTemplateDynamicData/update-widget-template-and-name.json`

## Changed Requests

- All former requests were renamed and moved into the module folders above.
- `Create Widget Template` now uses the Hello World template from the Widget Template lab.
- `Create Widget` and `Create Placement` now use the request bodies from the Widgets and Placements labs.
- `Create Placement` now targets the `home-top` region instead of `header_bottom`.
- Update requests now send descriptive example names instead of `Update Test`.

## Conventions

- Dynamic URL values are path variables (`:widget_template_uuid`, `:widget_uuid`, `:placement_uuid`) that can be edited on the Params tab, replacing placeholder strings such as `WIDGET_TEMPLATE_UUID`. They default to `{{widget_template_uuid}}`, `{{widget_uuid}}` and `{{placement_uuid}}`, except `Update Widget Template (New Version)`, whose path variable is left blank because it targets a template published with Widget Builder.
- Headers now match the other course collections: `Accept`, `Content-Type` and `X-Auth-Token`. The `X-Auth-Client` header was removed.
- Request bodies use JSON syntax highlighting.

## Automation

- The collection pre-request script stops a request with a clear message if `store_hash` or `v3_token` is not set in the active environment.
- Create requests save the new UUID to the `widget_template_uuid`, `widget_uuid` or `placement_uuid` environment variable, so later requests and request bodies are filled in automatically.
- Delete requests clear the matching environment variable.
- Every request has a test script that checks for an error-free response and the expected `data` shape.
