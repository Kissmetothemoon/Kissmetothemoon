*Efficient LLM inference, from algorithms to silicon.*

[![Homepage](https://img.shields.io/badge/Homepage-kissmetothemoon.github.io-4362F6?style=flat)](https://kissmetothemoon.github.io)
[![Google Scholar](https://img.shields.io/badge/Google_Scholar-Profile-4285F4?style=flat&logo=googlescholar&logoColor=white)](https://scholar.google.com/citations?user=3PW4loAAAAAJ)
[![Xiaohongshu](https://img.shields.io/badge/Xiaohongshu-小红书-FF2442?style=flat)](https://www.xiaohongshu.com/user/profile/68cba2df000000002102beb5)
[![Email](https://img.shields.io/badge/Email-Contact_Me-6A5ACD?style=flat)](mailto:yanruo.f@gmail.com)

### 👋 About me

I'm a PhD student at **Beihang University** and an intern at **ByteDance-PH**. I study how to make language model inference faster across languages and more reliable on analog hardware.

- **DATE 2027** accepted our paper on diffusion language models for analog in-memory computing. In hybrid measurements on a 16-chip eFlash system, diffusion models tolerated 1.4–3× as much weight noise as comparable autoregressive models. [Read the paper on arXiv](https://arxiv.org/abs/2611.32223).
- **WorldDraft** studies why parallel drafting speeds up English much more than Telugu. We trace part of the gap to words split across many tokens and use word-continuation counts to guide the draft. Preprint coming soon. [Project page and interactive demo](https://kissmetothemoon.github.io/worlddraft-page/) · [Code](https://github.com/Kissmetothemoon/WorldDraft)

I also enjoy photography. [Xiaohongshu](https://www.xiaohongshu.com/user/profile/68cba2df000000002102beb5) · [Douyin](https://www.douyin.com/user/self?from_tab_name=kissmetothemoon)

Contact me at **yanruo.f@gmail.com** or **ynfeng@buaa.edu.cn**.

<!-- 可选：贡献蛇形动画（由 .github/workflows/snake.yml 每日自动生成）。
     学术风做减法时可整段删除。 -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Kissmetothemoon/Kissmetothemoon/output/github-snake-dark.svg"/>
  <img alt="github contribution snake animation" src="https://raw.githubusercontent.com/Kissmetothemoon/Kissmetothemoon/output/github-snake.svg"/>
</picture>

### 🔍 Research Interests

- **Efficient decoding.** I work on speculative verification, multilingual drafting, and choosing which tokens to commit at each step of diffusion decoding. [ASD](https://arxiv.org/abs/2608.03447) · [WorldDraft](https://kissmetothemoon.github.io/worlddraft-page/) · [SetCommit](https://github.com/Kissmetothemoon/SetCommit)
- **Analog in-memory computing.** My hardware work studies how weight noise affects generation, expert routing, and the KV cache. Earlier projects explored noise-aware training and hybrid projection decomposition. [Publications](https://kissmetothemoon.github.io/publications/) · [ROMER](https://arxiv.org/abs/2605.11800) · [KV cache protection](https://arxiv.org/abs/2607.29076)

### ⚡ Featured Open Source

**WorldDraft** adds word-continuation counts to a parallel drafter before verification. On Qwen3-8B, it raises single-request speedup in Telugu from 1.08× to 1.62× with public DFlash. [Code and results](https://github.com/Kissmetothemoon/WorldDraft) · [Interactive demo](https://kissmetothemoon.github.io/worlddraft-page/#block-demo)

**[ASD](https://github.com/Kissmetothemoon/ASD)** — Approximate Speculative Decoding acceptance policy ([arXiv:2608.03447](https://arxiv.org/abs/2608.03447)).
Relaxes strict greedy verification by admitting draft tokens whose regret stays within a per-request bounded budget; exact verification is recovered at budget B = 0. Apache-2.0.

**[SetCommit](https://github.com/Kissmetothemoon/SetCommit)** — coordinated token commitments for few-step diffusion LM decoding ([blog post](https://kissmetothemoon.github.io/blog/2026/setcommit-coordinated-token-commitments/)).
Training-free set-selection layer that coordinates *which* tokens commit at each denoising step; +7.4 pp accuracy at 32 NFE and 1.44–1.74x geometric-mean speedup on LLaDA-8B / Dream-7B. MIT.

**[ASD for Transformers](https://huggingface.co/ynFeng/approximate-speculative-decoding)** — ASD as a Hugging Face [`custom_generate`](https://huggingface.co/ynFeng/approximate-speculative-decoding) method (transformers 5.19.x), token-identical to strict verification at B = 0.
```python
model.generate(..., assistant_model=draft,
    custom_generate="ynFeng/approximate-speculative-decoding", trust_remote_code=True,
    assistant_asd_budget=2.0, assistant_asd_local_ratio=0.25, assistant_asd_max_mismatches=2)
```

### 📝 Latest Blog Posts

<!-- BLOG-POST-LIST:START -->- [SetCommit: Coordinating Parallel Token Commitments in Few-Step Diffusion Language Models](https://kissmetothemoon.github.io/blog/2026/setcommit-coordinated-token-commitments/) (2026-10-22)
- [ASD: Trading a Bounded Regret Budget for Faster Speculative Decoding](https://kissmetothemoon.github.io/blog/2026/asd-bounded-regret/) (2026-09-02)
<!-- BLOG-POST-LIST:END -->
*(auto-updated daily from [my homepage](https://kissmetothemoon.github.io) via GitHub Actions)*


