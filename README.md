# Putting a Name to Your Soil — Decision Trees

Four independent trees: walkover test, hand (texture) test, pit test, and weed/pH indicators.

## Walkover test

```mermaid
flowchart TD
  A[Walk the plot on a moist day, plants actively growing] --> B{30+ stones per sq yard?}
  B -->|Yes| STONY(["Stony soil"])
  B -->|No| C{Dark brown/grey, rich in plant remains, spongy?}
  C -->|Yes| PEATY(["Peaty soil"])
  C -->|No| NONE(["No stony/peaty signs — go to hand test"])
```

## Hand test (texture)

```mermaid
flowchart TD
  A{Sticky on a wet day — clings to boots in large lumps?}
  A -->|No| B[Pick up a handful, moisten if dry, knead to break down lumps]
  B --> C{Feels or sounds gritty?}
  C -->|Yes| D{Possible to roll into a ball?}
  D -->|No| SAND(["Sand"])
  D -->|Yes| E{Difficult to make a ball and get it to stick together?}
  E -->|Yes| LOAMYSAND(["Loamy sand"])
  E -->|No| SANDYLOAM(["Sandy loam"])
  C -->|No| F{Form a ball — is it weak, easily broken, silky or soapy?}
  F -->|Yes| SILTLOAM(["Silt loam"])
  F -->|No| G[Strong ball — squeeze between finger and thumb]
  A -->|Yes| G
  G --> H{Surface becomes shiny?}
  H -->|No| I{Hard to reshape the ball; rolls out into threads?}
  I -->|Yes| CLAYLOAM(["Clay loam"])
  I -->|No| MEDIUMLOAM(["Medium loam"])
  H -->|Yes| J{Also gritty, very sticky when wet?}
  J -->|Yes| SANDYCLAY(["Sandy clay"])
  J -->|No| CLAY(["Clay"])
```

## Pit test

Dig a pit 2 ft × 2 ft × 2 ft on a moist day. The three checks are independent — any "Yes" gives its result.

```mermaid
flowchart TD
  A[Dig pit 2x2x2 ft] --> B{Topsoil dark, white subsoil a few inches below?}
  B -->|Yes| CHALKY(["Chalky soil"])
  A --> C{Hard sub-surface pan present, texture of baked clay?}
  C -->|Yes| POORDRAIN1(["Poorly-drained soil"])
  A --> D{Blue-grey or rusty brown streaks in subsoil?}
  D -->|Yes| POORDRAIN2(["Poorly-drained soil"])
```

## Weeds & pH indicators

Read directly from what's already growing — each check is independent.

```mermaid
flowchart TD
  A[Observe the plot's weeds and plants]
  A --> B{Rushes/sedges present, or moss/green slime on surface?}
  B -->|Yes| POORDRAIN(["Poorly-drained soil"])
  A --> C{Dock, thistle, daisy, plantain, creeping buttercup present — or rhododendron/azalea/heather/camellia thriving?}
  C -->|Yes| ACID(["Acid soil"])
  A --> D{Clover present — or rhododendron/azalea/camellia leaves yellowing?}
  D -->|Yes| ALKALINE(["Alkaline soil"])
  A --> E{Stinging nettle, sow-thistle, fat-hen, chickweed, groundsel present?}
  E -->|Yes| FERTILE(["Fertile soil"])
```
