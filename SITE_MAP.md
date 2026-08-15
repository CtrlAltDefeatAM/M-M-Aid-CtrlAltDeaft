# MMAid Web Site Map

```text
/
├── Home
│   ├── What MMAid does
│   ├── Supported files
│   └── Upload Character
│
├── #review
│   ├── File Drop
│   ├── Format Detection
│   ├── Import Preview
│   ├── Character Review
│   └── Download Report
│
├── #rules
│   ├── Action Economy
│   ├── Combat Maneuvers
│   ├── Hero Points
│   ├── Extra Effort
│   ├── Attacks
│   ├── Defenses
│   ├── Conditions
│   └── Character Rules
│
└── #privacy
    └── Local browser parsing
```

## Planned Phase 2

```text
/builder
├── Concept
├── Power Level / PP
├── Abilities
├── Defenses
├── Skills
├── Advantages
├── Powers
├── Attacks
└── Final Review

/tools
├── Attack / Effect Calculator
├── Defense Calculator
├── Combat Maneuver Calculator
└── PP Calculator
```

## Architecture

```text
Mastermind Maker .mm3 ─┐
Foundry Actor JSON ─────┤
Hero Lab XML ───────────┤
Generic JSON ───────────┼──> Web Adapter
Text Statblock ─────────┘        │
                                 ▼
                        Normalized Character
                                 │
                                 ▼
                           MMAid Core
                     (future shared extraction)
                                 │
                                 ▼
                        Validation + PlayerFix
                                 │
                                 ▼
                           Review Results
```
