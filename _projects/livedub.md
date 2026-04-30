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
  .post article p, .post article li, .post article blockquote { font-family: 'Source Serif 4', Georgia, serif; font-size: 1.1rem; line-height: 1.8; }
  .post article h1, .post article h2, .post article h3 { font-family: 'Inter', sans-serif; }
  .post article h2 { font-size: 1.5rem; font-weight: 600; margin-top: 2rem; }
  .paper-title { font-family: 'Inter', sans-serif; font-size: 2.5rem; font-weight: 700; }
  .paper-subtitle { font-family: 'Inter', sans-serif; font-size: 2rem; font-weight: 400; }
  .paper-btn { font-family: 'Inter', sans-serif; display: inline-block; margin: 0 4px 8px; padding: 6px 16px; border: 1px solid #aaa; border-radius: 4px; color: #555; font-size: 0.875rem; text-decoration: none; }
  .paper-btn:hover { background: #f0f0f0; text-decoration: none; color: #333; }
  .paper-btn.disabled { color: #aaa; border-color: #ddd; pointer-events: none; }
  .results-block { margin: 2.5rem 0 3rem; }
  .results-tag { display: inline-block; font-family: 'Inter', sans-serif; font-size: 0.7rem; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: #fff; background: #444; border-radius: 3px; padding: 2px 8px; margin-bottom: 0.5rem; }
  .results-tag.tag-clean { background: #2c7a4b; }
  .results-tag.tag-occ   { background: #7a4f2c; }
  .results-tag.tag-cross { background: #2c4a7a; }
  .results-desc { font-family: 'Inter', sans-serif; font-size: 1rem; font-weight: 600; color: #222; margin: 0 0 0.75rem; }
  .method-labels { display: flex; width: 100%; margin-bottom: 4px; }
  .method-labels span { flex: 1; text-align: center; font-family: 'Inter', sans-serif; font-size: 0.75rem; font-weight: 600; color: #555; }
  .method-labels span.ours { color: #c0392b; }
  .wide-video-wrap { width: 100%; overflow-x: auto; -webkit-overflow-scrolling: touch; }
  .wide-video-wrap video { width: 100%; min-width: 720px; display: block; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.12); }
  .video-item + .video-item { margin-top: 6px; }
  .teaser-wrap img { width: 100%; display: block; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.10); }
  .teaser-caption { font-family: 'Source Serif 4', Georgia, serif; font-size: 0.88rem; line-height: 1.65; color: #444; margin-top: 0.6rem; }
  .teaser-caption .fig-label { font-family: 'Inter', sans-serif; font-weight: 700; color: #222; }
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

<div class="teaser-wrap mb-2">
  <img src="/assets/img/publication_preview/livedub.png" alt="LiveDub teaser" loading="eager">
</div>
<p class="teaser-caption">
  <span class="fig-label">Figure 1.</span>
  We present LiveDub, a real-time audio-driven lip synchronization system for live streaming.
  Audio2Geometry generates spatially aligned geometry priors from audio and source video;
  Geometry2Pixel synthesizes the lip-synchronized output from these priors;
  TRN refines dental details as a plug-and-play module.
  LiveDub demonstrates accurate lip synchronization, high-fidelity tooth reconstruction,
  and real-time inference at 50+ FPS on a single GPU.
</p>

---

## Abstract

Audio-driven lip synchronization holds broad potential for live streaming, yet existing methods remain impractical due to three limitations: inpainting failures under foreground occlusions (e.g., microphones), inference latency incompatible with real-time constraints, and degraded tooth textures. Therefore, we present **LiveDub**, a real-time audio-driven lip synchronization system. To address these three challenges, LiveDub incorporates three targeted designs: (1) an occlusion-aware reference selection strategy that provides perioral priors robust to foreground occluders; (2) a reference masking strategy with a pixel-space tooth refinement network to eliminate shortcut artifacts and restore dental details; and (3) UNet3DMamba, a 3D hybrid backbone replacing quadratic attention with linear-complexity state-space modeling for real-time throughput with temporal consistency. LiveDub achieves 50 FPS on a single RTX 4090. Extensive experiments demonstrate significant improvements over state-of-the-art methods, making LiveDub the first framework to simultaneously deliver occlusion robustness, high-quality tooth synthesis, and real-time inference.

---


## Results

<!-- ── Clean Scene (tooth) ───────────────────────────────── -->
<div class="results-block">
  <div><span class="results-tag tag-clean">Clean Scene</span></div>
  <p class="results-desc">Frontal videos with high-fidelity tooth synthesis</p>
  <div class="method-labels">
    <span>Ground Truth</span>
    <span class="ours">LiveDub (Ours)</span>
    <span>LatentSync</span>
    <span>KeySync</span>
    <span>MuseTalk</span>
    <span>Diff2Lip</span>
    <span>VideoRetalking</span>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/tooth/tooth_1012.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/tooth/tooth_11322.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/tooth/tooth_14619.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/tooth/tooth_16550.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/tooth/tooth_459.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>

<!-- ── Occlusion Scene ───────────────────────────────────── -->
<div class="results-block">
  <div><span class="results-tag tag-occ">Occlusion Scene</span></div>
  <p class="results-desc">Videos with foreground occlusions (e.g., microphones)</p>
  <div class="method-labels">
    <span>Ground Truth</span>
    <span class="ours">LiveDub (Ours)</span>
    <span>LatentSync</span>
    <span>KeySync</span>
    <span>MuseTalk</span>
    <span>Diff2Lip</span>
    <span>VideoRetalking</span>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/occ/occ_10037.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/occ/occ_13819.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/occ/occ_14601.mp4" type="video/mp4">
      </video>
    </div>
  </div>
  <div class="video-item">
    <div class="wide-video-wrap">
      <video controls playsinline>
        <source src="/assets/video/livedub/occ/occ_8101.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>

<!-- ── Cross-Audio Dubbing ───────────────────────────────── -->
<div class="results-block">
  <div><span class="results-tag tag-cross">Cross-Audio Dubbing</span></div>
  <p class="results-desc">Driving a target video with a mismatched audio source</p>
  <div class="method-labels">
    <span>Ground Truth</span>
    <span class="ours">LiveDub (Ours)</span>
    <span>LatentSync</span>
    <span>KeySync</span>
    <span>MuseTalk</span>
    <span>Diff2Lip</span>
    <span>VideoRetalking</span>
  </div>
  <div class="wide-video-wrap">
    <video autoplay muted loop playsinline>
      <source src="/assets/video/livedub/cross_audio.mp4" type="video/mp4">
    </video>
  </div>
</div>

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
