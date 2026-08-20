# Laundry Decoder

Decode laundry care symbols from text descriptions, build a safe wash plan for a mixed load (color-bleeding risk, temperature ceilings, fabric conflicts), and get evidence-based stain removal protocols for 21 stain types.

## What it gives you

- **Care symbol decoding**: 30+ ISO 37500/GINETEX symbols described in words ('tub 40', 'square circle 2 dots', 'circle p', 'triangle crossed') → meaning + practical how-to
- **Load planner**: partitions a pile of garments into the fewest *safe* loads — bleeders isolated, delicates grouped, temperature ceilings respected — with per-load cycle advice
- **Stain first aid**: 21 protocols (red wine, blood, ink, grass, pet urine, wax, dye transfer...) ordered least-destructive-first, with protein-stain and fiber-specific warnings
- Batch-friendly JSON output for agents

## Use it when

- "What does this care label actually mean?"
- "Can I wash these together, and at what temperature?"
- "How do I get red wine out of cotton without setting the stain?"

## Quick start

```bash
python3 scripts/laundry_decoder.py decode "tub 40 with bar" "square circle 2 dots" "circle p"
python3 scripts/laundry_decoder.py plan \
  --item "white towels;white;60;cotton" --item "red tee;red;30;cotton" \
  --item "wool sweater;dark;30;wool" --item "silk blouse;light;30;silk"
python3 scripts/laundry_decoder.py stain "red wine" --fabric cotton
```

MIT © 2026 Denis Voronin
