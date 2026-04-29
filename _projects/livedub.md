---
layout: page
title: "LiveDub"
description: "Real-Time Lip Sync via MambaUNet with Plug-and-Play Dental Refinement"
img: assets/img/publication_preview/livedub.png
importance: 1
category: work
hide_navbar: true
_styles: >
  @font-face { font-family: 'Inter'; font-style: normal; font-weight: 400; src: url('/assets/fonts/Inter-Regular.woff2') format('woff2'); }
  @font-face { font-family: 'Inter'; font-style: normal; font-weight: 600; src: url('/assets/fonts/Inter-SemiBold.woff2') format('woff2'); }
  @font-face { font-family: 'Inter'; font-style: normal; font-weight: 700; src: url('/assets/fonts/Inter-Bold.woff2') format('woff2'); }
  @font-face { font-family: 'Source Serif 4'; font-style: normal; font-weight: 400; src: url('/assets/fonts/SourceSerif4-Regular.woff2') format('woff2'); }
  @font-face { font-family: 'Source Serif 4'; font-style: normal; font-weight: 600; src: url('/assets/fonts/SourceSerif4-SemiBold.woff2') format('woff2'); }
  @font-face { font-family: 'Source Serif 4'; font-style: italic; font-weight: 400; src: url('/assets/fonts/SourceSerif4-Italic.woff2') format('woff2'); }
  .post-header { display: none; }
  .post article { font-family: 'Source Serif 4', Georgia, serif; font-size: 1.1rem; line-height: 1.8; }
  .post article h1, .post article h2, .post article h3 { font-family: 'Inter', sans-serif; }
  .post article h2 { font-size: 1.5rem; font-weight: 600; margin-top: 2rem; }
  .paper-title { font-family: 'Inter', sans-serif; font-size: 2.5rem; font-weight: 700; }
  .paper-subtitle { font-family: 'Inter', sans-serif; font-size: 2rem; font-weight: 400; }
  .paper-btn { font-family: 'Inter', sans-serif; display: inline-block; margin: 0 4px 8px; padding: 6px 16px; border: 1px solid #aaa; border-radius: 4px; color: #555; font-size: 0.875rem; text-decoration: none; }
  .paper-btn:hover { background: #f0f0f0; text-decoration: none; color: #333; }
  .paper-btn.disabled { color: #aaa; border-color: #ddd; pointer-events: none; }
---

<div class="text-center mb-4">
  <h1 class="paper-title">LiveDub</h1>
  <h5 class="paper-subtitle">Real-Time Lip Sync via MambaUNet with Plug-and-Play Dental Refinement</h5>
  <p class="text-muted mt-1"><em>Anonymous Authors</em></p>

  <div class="mt-3 mb-4">
    <a class="paper-btn" href="https://arxiv.org/" target="_blank">📄 Paper</a>
    <a class="paper-btn" href="https://github.com/" target="_blank">💻 Code</a>
    <!-- <a class="paper-btn" href="#" target="_blank">🎬 Video</a> -->
  </div>
</div>

<div class="row justify-content-center mb-5">
  <div class="col-sm-10">
    {% include figure.liquid
      loading="eager"
      path="assets/img/publication_preview/livedub.png"
      title="LiveDub teaser"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

---

## Abstract

Audio-driven lip synchronization holds broad potential for live streaming applications. However, existing methods remain impractical for real-world deployment due to three critical limitations: inpainting failures caused by foreground occlusions (e.g., microphones), inference latency incompatible with real-time constraints, and degraded tooth textures in generated frames.

Therefore, we present **LiveDub**, a real-time audio-driven lip synchronization system tailored for live streaming. To address these three challenges, **LiveDub** incorporates three targeted designs:
(1) an occlusion-aware reference frame selection strategy that provides perioral texture priors preserving foreground occluder information for robust synthesis under occlusion;
(2) a reference masking strategy coupled with a pixel-space tooth refinement network to eliminate reference shortcut artifacts and restore fine-grained dental details; and
(3) UNet3DMamba, a 3D hybrid backbone replacing quadratic-complexity attention with linear-complexity state-space modeling to achieve real-time throughput while maintaining temporal consistency.

**LiveDub** achieves 50 FPS on a single RTX 4090. Extensive experiments demonstrate significant improvements over state-of-the-art methods, making **LiveDub** the first framework to simultaneously deliver occlusion robustness, high-quality tooth synthesis, and real-time inference.

---

## Method

<!-- TODO: replace with pipeline figure -->

LiveDub consists of two decoupled components:

**MambaUNet Backbone.** &nbsp; TODO — brief description of architecture.

**Plug-and-Play Dental Refinement.** &nbsp; TODO — brief description of the dental module and how it attaches.

---

## Qualitative Results

<!-- TODO: add comparison figures / video embeds -->

---

## Quantitative Results

<!-- TODO: add results table -->

---

<!-- ## BibTeX

```bibtex
@inproceedings{livedub2026,
  title     = {LiveDub: Real-Time Lip Sync via MambaUNet
               with Plug-and-Play Dental Refinement},
  author    = {Anonymous Authors},
  booktitle = {Under Review},
  year      = {2026}
}
``` -->
