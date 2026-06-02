# Decoder of the Encoder

> This is an amateur engineering project. We are not HPC professionals and make no competitive claims. Errors likely.

Bach's BWV 847 — the C-minor fugue from *The Well-Tempered Clavier*, Book I (1722) — laid out as a navigable graph tree. Each voice is a branch, each note is a leaf. You scroll, click, and the structure of the fugue becomes a place you can walk through.

**Open `rank-sphere.html` in a browser. Type `847`.**

## What it does

A fugue is, by construction, the same musical idea repeated across several voices, each transformed (transposed, inverted, augmented, delayed). This visualization treats those voices as branches of a tree:

- click a node to descend into a voice's subtree;
- breadcrumb navigation walks back up;
- as the audio plays, the corresponding nodes light up;
- a Penrose-chainmail "curtain" parts on entry; fiber-optic light strands trace voice entries through the tree;
- everything renders in a single self-contained HTML file — no build step, no dependencies.

The point is not the visual effect. The point is that you can navigate the structure of a 1722 piece of music as if it were a graph, and the navigation is faithful to what's actually in the score.

## Why it matters (DRT angle)

This is the **most concrete instantiation** of the Distributed Reconstruction framework. The fugue subject is the original signal $f$. Each voice is one partial observer with its own projection (transposition, inversion, augmentation). The whole fugue is the aggregate. What makes the fugue interesting is exactly the question the paper asks: the aggregate is not just a superposition of the parts — the contrapuntal relations across voices carry structure that no single voice carries alone.

The honest, current claim from the v0.1 draft is *not* that "the fugue has more norm than the subject" — that earlier formula has been retracted. The current claim is conditional: under a bounded computational budget, the aggregate exposes structure that the subject alone within the same budget does not. The fugue is a 300-year-old example of that pattern in audible form.

```
R(f) = Σ φᵢ · Cᵢ(Πᵢ f)
```

is the form of the aggregate. The framework around it — what counts as the budget, what "exposes structure" means precisely — is the work of the v0.1 paper.

## How to run

Single HTML file. Open in any modern browser. Audio is opt-in.

```
git clone https://github.com/norayr-m/decoder-of-the-encoder.git
open decoder-of-the-encoder/rank-sphere.html
```

Then type `847`.

## Structure

- `rank-sphere.html` — the visualization
- `docs/how-it-works.md` — fugue voices → tree branches mapping
- `docs/drt-connection.md` — link to the underlying paper
- `index.html` — landing
- `LICENSE`

## References

- Bach, J. S. — *The Well-Tempered Clavier*, Book I, BWV 847 (1722).
- Distributed Reconstruction work — v0.1 in preparation, N. Matevosyan and A. Petrosyan.
- Escher, M. C. — for the impossible-triangle aesthetic.

Visualizations co-authored with Claude (Anthropic).

## Author

Norayr Matevosyan

## License

Apache 2.0
