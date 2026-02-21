# compositional-flow-toward-cat

Evaluates whether a photograph's visual composition — its lines, light, and spatial arrangement — creates flow that converges on the cat subject. Scores high when geometry, tonal structure, and visual hierarchy align to make the cat the image's inevitable destination; scores low when the eye wanders or is pulled elsewhere.

## Purpose

Not every photograph of a cat is compositionally *about* the cat. A cat can sit squarely in a frame and still feel incidental — upstaged by a bright window, lost in a busy pattern, ignored by every line in the room. This function measures the difference between a photograph where a cat merely appears and one where the entire visual architecture of the image delivers the viewer's eye to the cat with a sense of inevitability.

The function does not evaluate whether the cat is cute, in focus, well-lit in isolation, or centrally placed. It evaluates whether the compositional forces at work in the photograph — the geometry, the tonal landscape, the spatial hierarchy — are working *for* the subject. It reads the image as a map of visual currents and asks: do those currents converge on the cat?

## Input

| Field | Type | Required | Description |
|---|---|---|---|
| `photograph` | `image` | Yes | A photograph containing a cat. The image may be of any style, setting, or quality — a composed portrait, a casual snapshot, indoor or outdoor, cluttered or minimal. The function analyzes the visual relationships within the image relative to the cat subject. |

## Output

A scalar score between **0** and **1**.

| Score Range | Interpretation |
|---|---|
| **0.8 – 1.0** | The composition powerfully converges on the cat. Lines, light, and spatial hierarchy all align to make the cat the unmistakable destination of the viewer's eye. The image feels as if it were built around the subject. |
| **0.6 – 0.8** | The composition favors the cat. Most visual forces support the subject, though minor competing elements or neutral zones prevent total convergence. The cat is clearly the primary focal point. |
| **0.4 – 0.6** | The composition is mixed. Some forces lead toward the cat while others are neutral or mildly competing. The cat is present but not decisively prioritized by the image's visual architecture. |
| **0.2 – 0.4** | The composition weakly supports the cat or is largely indifferent to it. The eye may find the cat eventually, but the image's lines, light, and spatial arrangement do not guide it there. |
| **0.0 – 0.2** | The composition actively works against the cat. Dominant lines lead elsewhere, brighter or higher-contrast areas pull the eye away, and competing focal points overshadow the subject. The cat is present but compositionally abandoned. |

## What It Evaluates

The function assesses three distinct qualities of compositional flow, each capturing a different dimension of how visual forces interact with the cat subject.

### 1. Linear Convergence

Do the lines and edges in the photograph point at the cat?

Every scene contains lines — floorboards, shelves, railings, architectural edges, shadow diagonals, surface boundaries. The human eye follows these lines involuntarily. Linear convergence measures whether the dominant lines in the image form a directional system that terminates at the cat.

- **High score:** Lines angle inward toward the cat from multiple directions. The cat sits at or near a vanishing point, at the end of a leading edge, or at the convergence of structural geometry. The environment appears to point at the subject.
- **Mid score:** Some lines approach the cat while others are neutral or unrelated. The geometry partially supports the subject but doesn't form a unified system.
- **Low score:** The dominant lines lead away from the cat, pulling the eye toward empty corners, competing objects, or out of the frame entirely. The geometry and the subject are in disagreement.

### 2. Tonal Pull

Does the distribution of light and contrast draw the eye toward the cat?

Light is attention. The eye is pulled to the brightest area in a scene, to zones of peak contrast, to places where luminance shifts most sharply. Tonal pull measures whether these tonal landmarks cluster around the cat or scatter to competing regions of the frame.

- **High score:** Light falls on the cat, contrast peaks at the subject, and surrounding areas are tonally subdued. The brightness gradient slopes toward the cat, creating a visual gravity well centered on the subject.
- **Mid score:** The cat receives some favorable light or contrast, but other areas carry comparable tonal weight. The pull toward the cat exists but isn't dominant.
- **Low score:** Brighter or higher-contrast areas exist elsewhere — a blazing window, a sunlit patch on the floor, a reflective surface. The tonal structure makes these competing zones more visually magnetic than the cat. The eye is drawn away from the subject.

### 3. Focal Resolution

Does the eye's journey through the image end at the cat?

A photograph is full of objects, textures, patterns, and colors, each competing for attention. Focal resolution measures whether this competition has a clear winner and whether that winner is the cat. It asks whether the viewer's gaze, after traveling through the frame, arrives at the cat with a sense of completion — or whether it wanders, bounces, or settles elsewhere.

- **High score:** The visual hierarchy is clear and resolves at the cat. Other elements serve as stepping stones, and the cat is the unmistakable destination. The viewer feels a sense of arrival.
- **Mid score:** The cat is the primary focal point but faces some competition. The eye mostly settles on the cat but occasionally drifts to a competing element before returning.
- **Low score:** Multiple focal points compete without resolution, or the eye settles on something other than the cat entirely. The image presents no clear visual hierarchy, or the hierarchy favors a different element. The cat is present but not prioritized.

## Use Cases

- **Photography curation:** Identify which cat photographs in a collection have the strongest compositional pull — the images where the scene itself seems to be looking at the cat, versus those where the cat is incidental to the frame.
- **Content ranking:** Rank cat photography by compositional quality for platforms, feeds, or galleries, distinguishing images with genuine visual magnetism from those that are merely adequate.
- **Photographic education:** Demonstrate how composition shapes the viewer's experience. Compare high-scoring and low-scoring images to illustrate how lines, light, and spatial hierarchy can make or break a subject's visual presence.
- **Portfolio feedback:** Give photographers a compositional signal on their cat photography — not whether the photo is good overall, but whether the composition is doing the work of directing attention to the subject.
- **Composite scoring:** Combine with other functions evaluating different aspects of cat photography (e.g., emotional expression, sharpness, background quality) to build a multidimensional assessment of image quality where compositional flow is one weighted factor.