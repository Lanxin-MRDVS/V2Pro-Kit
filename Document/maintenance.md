# V2 Pro Documentation and Release Maintenance

[Product Home](../README.md) / [Documentation](README.md) / Maintenance

## Preserve existing links

Keep the repository name, existing files, `Document/` and `img/` paths, Wiki page URLs, Release tags and asset filenames unchanged. Do not delete older documents or software. Organize access through indexes rather than moving published files. Preserve old README section anchors when changing headings.

## File ownership

| Location | Responsibility |
| --- | --- |
| `README.md` | Product overview, current packages in Release status, deployment steps, integration links and collapsed histories |
| `Document/README.md` | Index of current product documents, deployment guides and existing Wiki references |
| `Document/` | Published English PDF and Markdown documents; retain older editions here when superseded |
| `img/` | Shared brand assets, original product illustrations and existing guide images |
| `releases/README.md` | One consolidated English software changelog, newest version first |
| GitHub Releases | Software and related integration packages; no documentation-only release |
| Existing Wiki | Protocol and integration references at their original URLs |

Publish English customer-facing PDFs and Markdown. Do not upload Word sources or working drafts. Reuse original source illustrations; do not replace diagrams with page screenshots.

## Homepage presentation

Use the MRDVS English logo and keep the title centered. Do not add a separate row of navigation buttons. Place a short version-check reminder and two collapsed histories below the title, with no duplicated history tables at the bottom. The status card is the single current firmware download area. It shows the latest software packages and latest documentation separately. Keep upgrade conditions next to the package links and in the upgrade step.

Place each history anchor inside its `<details>` content after `<summary>`. In-page links target GitHub's rendered `#user-content-software-update-history` and `#user-content-document-update-history` IDs. Verify actual GitHub clicks, not just a local rendering with renamed IDs.

Use a concise Step / What to do / Guide table for the five deployment steps. Keep the original workflow illustration at 640 px. Use an aligned Tools and integration table for LxCameraViewer, optional QR resources, protocols and SDKs, identifying the relevant step. Do not repeat firmware downloads outside Release status. Keep the matching Frontend/Body warning visible and conditional firmware details in a disclosure. Retain detailed product reference material in a collapsed section. Give downloads clear component labels; retain the real filenames and original asset URLs.

## Software versioning

Keep release versions, Body versions, Frontend versions and embedded firmware versions distinct. Do not infer compatibility or release dates from package filenames. Use GitHub publication dates for the history table and retain differing build references as such.

For each new software release:

1. Confirm the delivered versions, component pairing and upgrade path.
2. Add the supplied changes to `releases/README.md`; never invent features, fixes or test results.
3. Publish packages under a new software Release without replacing older binaries.
4. Record package filenames, component roles, sizes, checksums when verified, and upgrade instructions.
5. Add a row to the homepage software history and update the current packages in the status card.
6. Verify asset links, guide links and the rendered page. Do not treat a documentation update as a firmware release.

Existing GitHub Release descriptions remain historical publication records. Maintain future consolidated English changes in the single Release Notes file and link the corresponding section from future Releases.

## Document versioning

Record the document's actual version and date, separately from its file refresh date. For an authorized in-place correction with an unchanged version, keep the filename and existing history row; add or update a file-refresh date when needed. For a new document version, retain the previous file and history row, then update current links.

Do not claim a product white paper proves all capabilities on every historical firmware package. Keep original deployment instructions available and identify their scope. Check product claims against the latest approved source, including conditions and limits.
