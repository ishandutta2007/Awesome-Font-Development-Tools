# Awesome-Font-Development-Tools

# Top Font Development Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Glyph Outline Editing, Variable Font Axes & Python-Driven Font Engineering*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Font Development Tools**. These tools help type designers and font engineers draw glyph outlines, define OpenType features, manage variable font axes, and compile source files into production-ready TTF, OTF, and WOFF2 fonts — with a spectrum running from polished commercial editors like Glyphs and FontLab to open-source editors and Python libraries that keep the entire pipeline on your own machine.

**Examples** include FontForge, BirdFont, fontTools, Fontra, and TruFont (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, scriptable font engineering, and browser-based editing — especially relevant as **FontForge remains the reference open-source font editor** with support for Type1, TrueType, OpenType, UFO, and CID-keyed formats [citation:5][citation:12], and **fontTools** provides the Python foundation that commercial editors and build pipelines rely on [citation:9].

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Glyphs** — **The macOS-native font editor standard.** Full glyph drawing, OpenType feature editing, variable font axis management, and a powerful Python API for automation. **One-time purchase** (~€249 for Glyphs 3, with upgrade pricing). **Trade-offs**: macOS-only, closed-source, and no browser or Linux version. **Best for professional type designers** wanting the most polished macOS font editing experience with deep scripting support.

- **FontLab** — **The cross-platform professional font editor.** Glyph drawing, hinting, variable fonts, and OpenType feature authoring on Windows and macOS. **One-time purchase** (~$499). **Best for designers** wanting a commercial editor that runs on Windows as well as Mac, accepting the one-time cost.

- **RoboFont** — **The UFO-native macOS editor for coders.** Built around the UFO format with a Python API and extension ecosystem. **One-time purchase** (~€199). **Best for type engineers** who want a hackable, UFO-centric editor with deep scripting.

- **Adobe Font Development Kit for OpenType (AFDKO)** — **The reference OpenType build toolkit.** Command-line tools for compiling and validating OpenType features. **Free from Adobe**. **Best for font engineers** needing Adobe's official feature file validation and compilation, often paired with an editor.

## Open-Source GitHub Projects

- **FontForge** — **The veteran open-source font editor.** **GPL-licensed**, available on Linux, Windows, and macOS, with support for **Type1, TrueType, OpenType, CFF, CID-keyed, SVG, UFO, and bitmap formats** [citation:5][citation:12]. **Full glyph drawing, outline editing, hinting, and OpenType feature support** — it is the most feature-complete free editor available. **Includes `fontlint` for validation and `sfddiff` for comparing font files** [citation:12]. **The honest caveat**: **the interface feels dated and idiosyncratic** — it has not been redesigned for modern workflows, and some operations (Remove Overlap with coincident splines, Expand Stroke near sharp bends) have known quirks [citation:5]. **Best for Linux users and budget-conscious designers** needing a complete font editor without licensing fees, accepting the interface friction.

- **BirdFont** — **The Vala-based font editor for outline creation.** **GNU GPL v3**, available on Linux, Windows, macOS, and BSD [citation:4][citation:11]. **Creates outline vector graphics and exports TTF, EOT, and SVG fonts** [citation:4][citation:11]. **Lighter than FontForge** with a more focused feature set for basic font creation. **The honest caveat**: **less feature-complete than FontForge** — no variable font support, limited OpenType feature editing, and a smaller ecosystem. **Best for beginners and simple font projects** where FontForge's complexity is overkill.

- **fontTools** — **The Python foundation for font engineering.** **MIT licensed**, **requires Python 3.11+**, with **no external dependencies beyond the standard library** [citation:9]. **The library every serious font pipeline uses**: `ttx` converts between OTF and XML, `pyftsubset` subsets fonts, `varLib` builds variable fonts from designspace files, and `feaLib` compiles OpenType features [citation:9]. **Supports reading and writing TrueType, OpenType, UFO, designspace, and AFM files** [citation:9]. **The honest caveat**: **it is a library and CLI toolkit, not an editor** — you need to write Python or pair it with an editor like FontForge. **Best for font engineers** building automated pipelines, validating fonts, or manipulating font binaries programmatically.

- **Fontra** — **The browser-based font editor.** **Open-source**, runs in the browser with a modern interface for glyph editing, spacing, and kerning. **Best for teams** wanting collaborative, browser-accessible font editing without installing desktop software, accepting that it is newer than FontForge or Glyphs.

- **TruFont** — **The streamlined, hackable UFO editor.** **Open-source**, built on the UFO format with Python scripting and a focus on simplicity. **The honest caveat**: **last updated in December 2025** per repository tracking, suggesting slower active development [citation:13]. **Best for designers** wanting a lighter UFO-native editor with scripting, accepting the maintenance uncertainty.

- **Shift** — **The modern Rust/TypeScript font editor.** **Open-source (Apache/MIT dual)**, cross-platform on macOS, Windows, and Linux, built with an Electron/TypeScript frontend and Rust core [citation:8]. **Supports drawing outlines, variable fonts (axes/sources/instances), components, and import/export of UFO, Designspace, Glyphs, and TrueType** [citation:8]. **MCP integration** lets Claude Code or Codex connect read-only to fonts open in Shift [citation:8]. **The honest caveat**: **alpha-stage** — kerning and text proofing are planned but not yet shipped, and workflows will change between releases [citation:8]. **Best for early adopters** wanting a modern, scriptable font editor with AI agent integration, accepting alpha-stage maturity.

- **Glyphr Studio** — **The beginner-friendly browser editor.** **Open-source**, aimed at **typeface design beginners and hobbyists** with a gentle learning curve [citation:14]. **Best for learning font design fundamentals** in the browser without installing software.

### Additional Strong Open-Source Options

- **Bezy** — **The Bevy-based font editor in Rust.** **Open-source (pre-v1.0 alpha)**, with UFO loading, WASM browser builds, and keyboard-driven editing [citation:1]. **Best for Rust developers and early adopters** wanting a native, GPU-rendered font editor, accepting that UI buttons for all features are not yet implemented [citation:1].

- **fontmake** — **The source-to-binary compiler.** **Open-source Python**, compiles UFO and Glyphs sources into OpenType and TrueType binaries, often paired with fontTools [citation:13]. **Best for build pipelines** turning design sources into production fonts.

- **fontFeatures** — **The feature file manipulation library.** **BSD-3-Clause**, provides a structured representation of OpenType features for programmatic manipulation — merging lookups, moving between languages, and authoring features without raw AFDKO syntax . **Best for font engineers** needing to edit feature files programmatically.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Font development tools differ significantly in editing depth, variable font support, and platform availability. **FontForge is the most complete open-source editor** but has a dated interface and known quirks in some outline operations [citation:5]. **BirdFont is simpler** but lacks variable font support [citation:4]. **fontTools is a library, not an editor** — it powers pipelines but requires scripting knowledge [citation:9]. **Shift and Bezy are alpha-stage** — evaluate stability before committing production work [citation:1][citation:8]. **TruFont's maintenance status is uncertain** as of late 2025 [citation:13]. **Commercial editors (Glyphs, FontLab, RoboFont) remain the polish leaders** for professional type design, with Glyphs being macOS-only.
- Self-hosted open-source solutions require proper Python environments for fontTools, build toolchains for Rust-based editors (Shift, Bezy), and awareness that variable font compilation requires mastering designspace files and interpolation-compatible masters.

---

**Made for type designers, font engineers, and developers choosing font development tools that match their platform, scripting needs, and budget.**
Let's make font development more open, scriptable, and standards-based.
