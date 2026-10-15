Public edition public.1 removes the shared COS credential envelope and requires each installer to configure their own storage. Upstream license conditions below remain in force.

# Third-party components

Hypit 0.2.17, commit 7f730abf72fa1e4a543eed8cd1807319d9f18196, is bundled as a fixed npm distribution. Its modified Apache 2.0 terms are retained in LICENSE and vendor package. Hypit branding and native reports are unchanged. This package is an internal single-organization beta; commercial redistribution or multi-tenant hosting is outside this delivery.

pyJianYingDraft, commit 6bb2d06a713f7b58e1375269daec835a03882086 (0.3.0), Apache-2.0, is retained in python/vendor with its license. Hypit-plus modifies its __init__.py to disable automatic import of the optional upstream Windows UI controller unless HYPIT_PLUS_ENABLE_UPSTREAM_UI=1. The exporter does not use that controller.

Project-owned VideoCopyer Ark Seedance, Seedream Pro, ranking and Last War components are copied with the user's authorization for independent internal development. They are not represented as third-party public-domain material. Existing source files and identifiers are preserved.

React, React DOM and React Flow are MIT-licensed; xmldom is MIT; esbuild is MIT. Their package licenses remain in the installed distribution. Exact npm versions and integrity hashes are in package-lock.json. Python packages are pinned in python/requirements.txt; v0.2 ships the Windows CPython 3.12 wheels already expanded with their license files. No Sim, FlowGram, AG-UI, n8n or jianying-ai-mcp implementation is copied into this plugin.

HyperFrames engine/producer 0.7.101 and their transitive packages are included with their original package licenses and the exact npm lock. Node 24.18.0 Windows x64 is bundled with runtime/NODE-LICENSE.


v0.2 bundles the offline draft core from https://github.com/luoluoluo22/jianying-editor-skill at commit 32c56928ded4f9e2c2b80e099dc7abb793d2c30b. Its MIT project license is in python/editor_vendor/JIANYING-EDITOR-LICENSE; the Apache-2.0 pyJianYingDraft license remains beside that core. Only automatic Windows controller import is disabled in __init__.py. videocopyer supplies its own safe revision adapter and does not use the upstream wrapper's recreation/overwrite behavior. Provenance is recorded in python/editor_vendor/PROVENANCE.json.

Python 3.12.10 Windows x64 embeddable package is bundled from python.org with its LICENSE.txt. Download SHA256: 4acbed6dd1c744b0376e3b1cf57ce906f9dc9e95e68824584c8099a63025a3c3. The pinned Windows CPython 3.12 dependencies from python/requirements.txt and their dist-info license files are included in python/deps. No Python executable from the Codex host or personal site-packages is distributed.


v0.3 adapts the active production instructions to direct API configuration and removes hosted-account recommendations. The original upstream Skill is retained in docs/upstream/hypit-skill-original.md. Native package identifiers, reports and licenses remain intact; UI attribution is available under the open-source-license disclosure. COS request signing follows https://cloud.tencent.com/document/api/436/7778; the implementation uses Node built-ins.

v0.4 adds an adapter that launches a separately installed Seed-VC V2 Python runtime. The adapter does not copy Seed-VC source, model weights or caches into this plugin. The tested external source is https://github.com/Plachtaa/seed-vc at commit 51383efd921027683c89e5348211d93ff12ac2a8, GPL-3.0; keep its LICENSE with any separate runtime. `docs/SEED-VC.md` describes the boundary. LivePortrait is named in production guidance as a local post-generation step; its source, weights and executable are not bundled here.
