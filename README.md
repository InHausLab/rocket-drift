# 🚀 Rocket Drift

A space flying game. Hold to thrust up, release to drift down. Avoid meteors and planets. Reach the portal.

## Play

**Live:** https://inhauslab.github.io/rocket-drift/

Or open `index.html` directly in any modern browser — no server needed.

## Controls

| Input | Action |
|-------|--------|
| Click / tap & hold | Thrust up |
| Spacebar (hold) | Thrust up |
| Release | Drift down |

## Adding New Levels

Find the `LEVELS` array near the top of the `<script>` tag in `index.html`. Add a new object following this template:

```javascript
{
  id: 6,
  name: 'Level Name',
  nebula: ['#hex1', '#hex2'],   // background gradient colors
  baseSpeed: 360,               // starting scroll speed (px/s)
  maxSpeed: 720,                // max scroll speed at level end
  length: 26000,                // world length in pixels
  meteorDensity: 1.5,           // higher = more meteors (0 = none)
  meteorMinR: 14,               // min meteor radius
  meteorMaxR: 44,               // max meteor radius
  planetDensity: 1.0,           // higher = more planets (0 = none)
  planetMinR: 60,               // min planet radius
  planetMaxR: 180,              // max planet radius
  bpm: 140,                     // music tempo
  musicKey: 'intense'           // 'chill' | 'mid' | 'intense'
}
```

Levels unlock progressively. Best times are saved in localStorage.
