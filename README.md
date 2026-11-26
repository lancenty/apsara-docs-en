# Alibaba Cloud Apsara Stack English Documentation — Markdown Edition

Curated English product documentation for **Alibaba Cloud Apsara Stack** converted into offline-readable Markdown and organized by release version, 11 categories, and product code.

## Versions & Scope

| Directory | Description | Documents |
| :--- | :--- | :---: |
| `V3.18.6/` | V3.18.6 release documentation | 189 |
| `V3.18.6_2607/` | v3.18.6-2607 release documentation | 176 |
| `legacy/` | Pre-3.18.6 retained docs (`eip`, `terraform`, `oss`, `sls`) | 8 |
| **Total** | `373` documents across `11` categories | **373** (`62,592` pages) |

## Categories (11)

`Cloud Platform`, `Compute`, `Storage`, `Network`, `Database`, `Middleware`, `Big Data`, `Security`, `Monitoring and O&M`, `DR and Migration`, `OpenTrek`

## Notes

- **Self-contained assets**: Each Markdown document stores its figures in an independent sibling `<assets_dir>/` directory (e.g. `en-ecs-user-guide-v3.18.6-20260630.assets/`) with WebP `q=90` compression (keeping original PNG when smaller), keeping working-tree size at `~515 MiB`.
- **Original PDF bundles**: Unmodified source PDFs are archived per version under [Releases (`pdf-v3.18.6`)](https://github.com/lancenty/apsara-docs-en/releases/tag/pdf-v3.18.6).
- **Verification**: [`manifest.json`](manifest.json) records per-document `document_id`, SHA-256 digests, and asset inventories; all `373` documents passed full CommonMark render and asset verification with `0` errors and `0` conflicts.

## Document IDs

Every `document_id` in `manifest.json` has six segments that mirror the release package layout:

```
{language}/{package_version}/{category}/{product_code}/{document_key}/{document_version}
```

For example, `OpenTrek/apsara_stack_platform/Apsara Uni-manager Apsara Copilot Product Introduction 20260828.pdf` published in the SP2607 bundle:

```
en-us/3.18.6_2607/opentrek/apsara_stack_platform/apsara-copilot-product-introduction/20260828
```

| Segment | Meaning | Example |
| :--- | :--- | :--- |
| `language` | Document language | `en-us` |
| `package_version` | Release package version and date (or `legacy`) | `3.18.6_2607`, `legacy` |
| `category` | Language-neutral category slug | `opentrek`, `compute`, `security` |
| `product_code` | Published product code | `opentrek`, `ecs`, `aegis` |
| `document_key` | Document topic, prefixed by product when a code covers several products | `apsara-copilot-product-introduction` |
| `document_version` | Eight-digit document version from the cover | `20260701` |

