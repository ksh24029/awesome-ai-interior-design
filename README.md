# Awesome AI Interior Design [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

A curated list of practical AI tools, open-source projects, model components, workflows, and research for interior design, home renovation, virtual staging, exterior visualization, and landscape design.

> **Status:** Last reviewed on **2026-08-20**. Entries are not ranked. This repository uses no affiliate or referral links.
>
> **Disclosure:** This list is maintained by the maker of ImagineMyHouse. The maintainer's product is clearly labeled and follows the same inclusion rules as every other entry.

## Contents

- [Choose the Right Workflow](#choose-the-right-workflow)
- [Hosted Tools](#hosted-tools)
  - [Room Redesign and Home Visualization](#room-redesign-and-home-visualization)
  - [3D Planning and Professional Rendering](#3d-planning-and-professional-rendering)
  - [Virtual Staging and Real-Estate Photos](#virtual-staging-and-real-estate-photos)
  - [Exterior, Paint, and Landscape Design](#exterior-paint-and-landscape-design)
- [Open-Source Projects](#open-source-projects)
  - [Reference Applications](#reference-applications)
  - [Models and Workflow Building Blocks](#models-and-workflow-building-blocks)
- [Reference Workflows](#reference-workflows)
- [Prompt Recipe](#prompt-recipe)
- [Evaluation Checklist](#evaluation-checklist)
- [Research and Datasets](#research-and-datasets)

## Choose the Right Workflow

| Goal | Typical workflow | What to prioritize |
| --- | --- | --- |
| Restyle a furnished room | Photo-to-photo room redesign | Geometry preservation, controllable style, edit history |
| Furnish an empty room | Virtual staging | Furniture scale, perspective, shadows, listing-policy compliance |
| Replace one object or material | Segmentation plus masked inpainting | Accurate masks, local edits, unchanged surroundings |
| Turn a sketch or floor plan into a render | 3D planning or edge-conditioned generation | Dimensions, camera consistency, editable output |
| Redesign a facade or garden | Domain-specific photo editing | Climate/context awareness, surface boundaries, structural fidelity |
| Build a production pipeline | Detection, segmentation, depth, conditioning, inpainting, quality checks | Repeatability, privacy, licensing, failure recovery |

## Hosted Tools

Commercial and hosted products are listed once in the category that best represents their primary workflow. Selection favors tools with a distinct, evaluable interior-design use case rather than generic image generators. Pricing changes frequently, so verify current plans on each provider's official site.

### Room Redesign and Home Visualization

- [Decor8 AI](https://www.decor8.ai/) - Multi-platform room redesign and virtual-staging tools built around photo uploads.
- [HomeDesignsAI](https://homedesigns.ai/) - Photo-based tools for interiors, exteriors, gardens, decluttering, material changes, and virtual staging.
- [Ideal House](https://ideal.house/) - Home-visualization platform with photo editing, floor-plan tools, furniture try-on, and a design community.
- [ImagineMyHouse](https://imaginemyhouse.com/) - Photo-based workflows for interior and exterior redesign, landscaping, virtual staging, and room cleanup. **Maintainer's project.**
- [Interior AI](https://interiorai.com/) - Room redesign, virtual staging, sketch or SketchUp rendering, and generated walkthrough workflows.
- [REimagineHome](https://www.reimaginehome.ai/) - Guided photo-to-design workflows for interiors, landscaping, virtual staging, and decluttering.
- [Renov](https://renov.space/) - Interactive room redesign with targeted edits, furniture replacement, and design guidance.
- [RoomGPT](https://www.roomgpt.io/) - A focused single-photo room-restyling tool for quick concept exploration.
- [Spacely AI](https://www.spacely.ai/) - Rendering and image-editing workspace for architects, interior designers, and real-estate teams.

### 3D Planning and Professional Rendering

- [Coohom](https://www.coohom.com/) - Browser-based 3D floor planning, furnishing, rendering, and walkthrough creation with AI-assisted workflows.
- [DecorMatters](https://decormatters.com/) - Mobile-first room planning and design community with AR, furniture placement, and AI makeovers.
- [Homestyler](https://www.homestyler.com/) - Web and mobile tools for floor plans, furnishing, 3D rendering, and AI-assisted design.
- [Planner 5D AI Studio](https://ai.planner5d.com/) - A workspace for turning floor plans, room photos, sketches, references, and prompts into design presentations.

### Virtual Staging and Real-Estate Photos

- [Apply Design](https://www.applydesign.io/) - AI and drag-and-drop staging for 2D and 360-degree photos, with furniture removal and multi-angle workflows.
- [Virtual Staging AI](https://www.virtualstagingai.app/) - One-click furnishing and furniture removal for property-listing photos.

Several tools in the room-redesign section also include virtual-staging modes; entries are kept in one category to avoid duplication.

### Exterior, Paint, and Landscape Design

- [Housepaint AI](https://housepaint.ai/) - Paint visualization for interior and exterior surfaces using photo-based surface detection.
- [Neighborbrite](https://neighborbrite.com/) - Landscape concepts, targeted yard edits, plant identification, and optional professional planning.
- [Virtual House Flip](https://www.virtualhouseflip.com/) - Interior and exterior property visualization from listing or uploaded photos.

Several tools in the room-redesign section also cover exterior and landscape workflows; entries are kept in one category to avoid duplication.

## Open-Source Projects

### Reference Applications

- [roomGPT](https://github.com/Nutlope/roomGPT) - An open-source Next.js reference application for photo-based room redesign.
- [Virtual Staging](https://github.com/mithunparab/virtual-staging) - A virtual-staging pipeline combining depth and edge guidance, ControlNet, Grounding DINO, SAM, and targeted inpainting.

### Models and Workflow Building Blocks

- [BrushNet](https://github.com/TencentARC/BrushNet) - A plug-and-play diffusion architecture for masked image inpainting.
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) - A node-based interface for building repeatable diffusion and image-editing workflows.
- [ControlNet](https://github.com/lllyasviel/ControlNet) - Spatial conditioning from edges, depth, segmentation, poses, and other structural guides.
- [Depth Anything V2](https://github.com/DepthAnything/Depth-Anything-V2) - Monocular depth estimation for geometry-aware conditioning and scene analysis.
- [Diffusers](https://github.com/huggingface/diffusers) - A model and pipeline library with inpainting, ControlNet, adapter, and image-to-image components.
- [Grounding DINO](https://github.com/IDEA-Research/GroundingDINO) - Open-vocabulary object detection for locating furniture and architectural elements from text labels.
- [Inpaint Anything](https://github.com/geekyutao/Inpaint-Anything) - A segmentation-assisted workflow for removing, replacing, or filling selected image regions.
- [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter) - Image-prompt conditioning that can be combined with text prompts and structural controls.
- [PowerPaint](https://github.com/open-mmlab/PowerPaint) - Task-aware inpainting for object removal, insertion, shape-guided editing, and outpainting.
- [SAM 2](https://github.com/facebookresearch/sam2) - Promptable image and video segmentation for producing editable masks.
- [Segment Anything](https://github.com/facebookresearch/segment-anything) - General-purpose promptable segmentation used by many object-removal and replacement pipelines.

## Reference Workflows

These are implementation patterns, not universal recipes. Model choice, control strength, masking strategy, and post-processing should be tested against your own image set.

### Geometry-Preserving Room Restyle

```text
Room photo
  -> depth map + edge/line map
  -> structural conditioning with ControlNet
  -> optional style reference with IP-Adapter
  -> generate several candidates
  -> repair local artifacts with masked inpainting
  -> compare against the original geometry
```

### Furniture or Material Replacement

```text
Room photo
  -> locate the target with Grounding DINO or a manual box
  -> generate a precise mask with SAM / SAM 2
  -> expand and feather the mask
  -> inpaint the selected region
  -> verify scale, perspective, contact shadows, and unchanged surroundings
```

### Empty-Room Virtual Staging

```text
Empty-room photo
  -> estimate depth and usable floor regions
  -> preserve walls, windows, doors, and ceiling boundaries
  -> generate furniture inside a constrained staging mask
  -> run object and geometry checks
  -> repair collisions, floating objects, and repeated furniture
```

### Sketch or Floor Plan to Render

```text
Sketch, line drawing, or plan
  -> clean line extraction
  -> edge or line conditioning
  -> text prompt + optional material/style reference
  -> render candidates
  -> localized edits instead of regenerating the whole image
```

## Prompt Recipe

A useful room-redesign prompt usually separates **design intent** from **preservation constraints**.

```text
[room type], [design goal], [style], [materials], [color palette],
[lighting], [furniture scale], [camera and lens description].

Preserve the existing walls, windows, doors, ceiling height, camera position,
perspective, and room proportions. Change only [target elements].
```

Example:

```text
Warm modern living room with light oak, walnut accents, textured plaster walls,
a low-profile neutral sofa, a wool rug, restrained decor, and soft indirect evening
lighting. Keep furniture realistically scaled for the room.

Preserve the existing architecture, windows, doorway locations, camera position,
perspective, and floor area. Do not add new openings or change the ceiling height.
```

Useful negative constraints:

```text
No warped walls, no extra windows or doors, no duplicated furniture, no floating
objects, no blocked walkways, no distorted perspective, no text, no watermark.
```

## Evaluation Checklist

Before treating a generated result as useful design evidence, check:

- **Structural fidelity:** Walls, openings, ceiling lines, and camera perspective still match the input.
- **Edit locality:** Areas outside the requested change remain stable.
- **Scale and placement:** Furniture proportions, clearances, and circulation paths are plausible.
- **Lighting:** New objects inherit believable direction, intensity, color temperature, and contact shadows.
- **Material behavior:** Wood grain, fabric, glass, metal, and reflective surfaces remain coherent.
- **Artifact rate:** Repeated objects, fused geometry, broken legs, impossible reflections, and unreadable details are limited.
- **Controllability:** Similar inputs and settings produce reasonably consistent results.
- **Operational fit:** Export resolution, privacy policy, retention period, commercial-use terms, and revision controls match the project.

## Research and Datasets

- [Adding Conditional Control to Text-to-Image Diffusion Models](https://arxiv.org/abs/2302.05543) - The ControlNet paper on adding spatial controls to diffusion models.
- [BrushNet: A Plug-and-Play Image Inpainting Model with Decomposed Dual-Branch Diffusion](https://arxiv.org/abs/2403.06976) - Mask-aware inpainting with separate branches for masked-image features and noisy latents.
- [Depth Anything V2](https://arxiv.org/abs/2406.09414) - Monocular depth estimation models and evaluation work.
- [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752) - The latent-diffusion foundation used by many image-generation and editing systems.
- [IP-Adapter: Text Compatible Image Prompt Adapter for Text-to-Image Diffusion Models](https://arxiv.org/abs/2308.06721) - Lightweight image-prompt conditioning compatible with text and structural controls.
- [Segment Anything](https://arxiv.org/abs/2304.02643) - Promptable segmentation for generating object and region masks.
- [InteriorNet](https://interiornetdataset.github.io/) - A large synthetic indoor-scene dataset with rendered imagery and sensor data.
- [Structured3D](https://structured3d-dataset.org/) - Photorealistic indoor scenes with rich 3D structure annotations.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

A good entry uses the official project URL, appears in one category, contains one neutral sentence explaining the practical use, and discloses any relationship between the contributor and the project.

