# Connection to the Distributed Reconstruction Theorem

## The Theorem

Given a collection of observers, each holding only a boundary projection Π_i of an unknown function f, the aggregate reconstruction:

```
R(f) = Σ φ_i · C_i(Π_i f)
```

satisfies `‖R(f)‖ > ‖f‖` when:
1. Observer projections span the function space (sufficient orthogonality)
2. At least one observer adds structure beyond pure recovery (non-trivial completion)
3. Completion preserves what the projection captured (faithfulness: Π∘C∘Π = Π)
4. Small updates produce small changes (Lipschitz continuity)

The excess is not more information — it is **computational accessibility**: the aggregate makes explicit what was implicit but not computable from any single projection.

## The Fugue as Instantiation

| DRT Concept | Fugue Mapping |
|---|---|
| f (unknown function) | The fugue subject — 4 bars of C minor |
| Π_i (boundary projection) | Voice entry: transposition, inversion, augmentation of the subject |
| C_i (internal completion) | Contrapuntal development: each voice extends beyond the subject using harmonic priors |
| φ_i (weights) | Voice prominence at each moment (soprano leads, bass grounds) |
| R(f) (aggregate) | The complete fugue — all 4 voices simultaneously |
| ‖R(f)‖ > ‖f‖ | The fugue exceeds the subject. Obviously. That's the whole point. |

## Three Types of Completion in Music

- **Type 1 (Recovery)**: The subject restated faithfully — tonic answer, exact repetition
- **Type 2 (Deduction)**: Countersubject, harmonic development, stretto — validly derived from the subject through contrapuntal rules (the observer's priors)
- **Type 3 (Hallucination)**: A wrong note. Bach doesn't have these. That's what makes him Bach.

## Why This Visualization

The graph tree makes the DRT structure *navigable*. You can see each observer (voice) in isolation. You can see them combine. You can watch the temporal unfolding — the >1 result happening in real time as voices enter and the reconstruction exceeds the subject.

The fugue proves the theorem by existing. The visualization lets you walk through the proof.

## Reference

Matevosyan, N., Anoian, C., Petrosyan, A. — *Distributed Reconstruction from Incomplete Boundary Projections with Non-Trivial Internal Completion* (2026, draft)
