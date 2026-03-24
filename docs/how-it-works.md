# How It Works

## Fugue → Graph

Bach's BWV 847 Fugue No.2 in C minor has 4 voices: soprano, alto, tenor, bass. The `fugue_to_graph()` function parses the musical structure into a tree:

- **Root node**: the complete fugue (rank 0)
- **Voice branches**: each voice becomes a subtree (rank 1)
- **Phrase groups**: subdivisions within each voice (rank 2+)
- **Leaf nodes**: individual notes — the atomic musical events

## Navigation

Click any node to descend into its subtree. The view recenters on the selected node's children. Breadcrumb trail at top-left tracks your position in the tree. Click breadcrumbs to navigate back up.

At every level, the rendering adapts:
- **Rank 0** (home): full view, center node visible, all voices as orbital branches
- **Rank 1** (voice): single voice expanded, siblings dimmed
- **Rank 2+** (phrases/notes): increasing detail, scaffolding geometry mutates toward Escher

## Temporal Layer

The fugue plays via Web Audio API. As notes fire:
- Their corresponding leaf nodes **glow** (golden pulse, exponential decay)
- **Fiber-optic light strands** trace from glowing leaves toward parent nodes
- The HUD shows current note, voice, and position in the fugue

The temporal glow makes the graph traversal feel alive — you're not just seeing the structure, you're seeing it *play*.

## The Gate

On load, Penrose impossible triangles fill the screen as a chainmail curtain. Semi-transparent — the honeycomb structure bleeds through underneath, sleeping.

Enter `847` (the BWV number). The triangles part to the sides like theater curtains, bunching at the edges. They never fully disappear — they stay as permanent fabric at the screen margins.

## Rendering

Everything is 2D Canvas with no external dependencies:
- Hexagonal cells for nodes (honeycomb topology)
- Golden color palette (rgba 240,192,64 base)
- Dark background (#1a1a2e)
- All geometry computed from node count and rank — self-similar at every scale
