# decoder-of-the-encoder

**Decomposition of THE composition by the decoder of the encoder.**

BWV 847 — Bach's Fugue No.2 in C minor from The Well-Tempered Clavier, Book I (1722) — mapped to a navigable graph tree.

The fugue is the natural encoding: **composition → decomposition → decompression**. The same function at every scale.

## What it does

Each voice becomes a branch. Each note becomes a leaf. The temporal structure of the fugue — subject entries, inversions, stretto — becomes a traversable topology. You navigate Bach as a tree.

**Open `rank-sphere.html` in a browser. Enter `847`.**

## Features

- **Graph-navigable tree**: click nodes to descend into voice subtrees, breadcrumb navigation back up
- **Temporal glow**: nodes illuminate when their notes fire in the audio timeline
- **Penrose chainmail curtain**: impossible triangles that part like theater fabric on entry
- **Fiber-optic light strands**: bright bursts trace voice entries through the tree
- **Rank-based rendering**: queen's warmth at every level, scaffolding mutates into Escher at depth
- **Self-contained**: single HTML file, no dependencies, no build step

## The math

This visualization is a concrete instantiation of the [Distributed Reconstruction Theorem](docs/drt-connection.md) — the framework for understanding how incomplete observers collectively reconstruct representations that exceed the original.

The fugue subject IS the function f. Each voice IS an observer with its own projection Π_i (transposition, inversion, augmentation). Bach IS the aggregate reconstruction operator R(f). The result exceeds the subject because each voice adds structure (Type 2: deduction) through contrapuntal priors that no single voice carries alone.

```
R(f) = Σ φ_i · C_i(Π_i f)    where ‖R(f)‖ > ‖f‖
```

The fugue proves the theorem by existing.

## Structure

```
rank-sphere.html              — the visualization (open in browser, enter 847)
docs/
  how-it-works.md             — graph mapping: fugue voices → tree branches
  drt-connection.md           — link to the Distributed Reconstruction Theorem
LICENSE
```

## References

- Bach, J.S. — *The Well-Tempered Clavier*, Book I, BWV 847 (1722)
- Matevosyan, N., Apidae, C., Petrosyan, A. — *Distributed Reconstruction from Incomplete Boundary Projections with Non-Trivial Internal Completion* (2026, draft)
- Escher, M.C. — for the impossible triangles that guard the gate

## Author

Norayr Matevosyan

## License

MIT
