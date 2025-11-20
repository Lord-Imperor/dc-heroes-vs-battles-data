# DC FRAMEWORK COMPLETE STAT MAPPING
## Full Integration of VS Battles + DC Universe Roleplay System

***

## OVERVIEW

This document provides the **definitive mapping** between VS Battles Wiki data and your DC Universe Roleplay Framework (0-25 scale).

### Core Stats (0-25 Scale)

**COMBAT STATS**:
- **Reflexes**: Reaction time, combat awareness
- **Movement**: Travel speed, positioning 
- **Power**: Striking force, damage output
- **Resilience**: Biological durability
- **Armor**: External protection

**DC MITIGATION STATS**:
- **Skills**: Training, technique, adaptability
- **Resourcefulness**: Gadgets, prep, improvisation

***

## VS BATTLES TIER → POWER MAPPING

### Human Level (0-3)
```
10-C: 0  (Below average)
10-B: 1  (Normal human)
10-A: 2  (Athletic human)
9-C:  3  (Peak human - street level)
```

### Enhanced Human (4-7)
```
9-B: 5   (Wall level)
9-A: 6   (Small building)
8-C: 8   (Building)
```

### Superhuman (8-12)
```
High 8-C: 9
8-B: 10  (Large building)
8-A: 12  (City block)
7-C: 12  (Town)
7-B: 13  (City)
7-A: 15  (Mountain)
```

### Powerhouse (13-19)
```
6-C: 16  (Island)
6-B: 17  (Country)
6-A: 18  (Continent)
5-C: 19  (Moon)
5-B: 21  (Planet)
5-A: 22  (Large planet)
```

### Cosmic (20-25)
```
4-C: 23  (Star)
4-B: 23  (Multi-star)
4-A: 24  (Solar system)
3-C: 24  (Galaxy)
3-B: 24  (Multi-galaxy)
3-A: 25  (Universe)
2-C: 25  (Multiverse)
1-A+: 25 (Beyond)
```

***

## VS BATTLES SPEED → REFLEXES/MOVEMENT

### Speed Scale Mapping
```
Below Average Human:      1,  1
Average Human:            2,  2
Athletic Human:           3,  3
Peak Human:               5,  5
Subsonic:                 8,  8
Subsonic+:                9,  9
Supersonic:              10, 10
Supersonic+:             11, 11
Hypersonic:              12, 12
High Hypersonic:         13, 13
Massively Hypersonic:    14, 14
Massively Hypersonic+:   15, 15
Sub-Relativistic:        16, 16
Relativistic:            17, 17
Relativistic+:           18, 18
FTL:                     18, 18
FTL+:                    19, 19
Massively FTL:           20, 20
Massively FTL+:          22, 22
Infinite/Immeasurable:   25, 25
```

**IMPORTANT**: Grounded characters (no flight/teleport) cap Movement at 5-8 even with high reflexes.

***

## VIP CHARACTER DATABASE

### S-TIER (Cosmic/Kryptonian)

#### **Superman**
```json
{
  "power": 21,
  "reflexes": 20,
  "movement": 22,
  "resilience": 21,
  "armor": 0,
  "skills": 10,
  "resourcefulness": 8,
  "tags": ["kryptonian", "flight", "solar_powered"]
}
```

#### **Wonder Woman**
```json
{
  "power": 18,
  "reflexes": 18,
  "movement": 16,
  "resilience": 18,
  "armor": 8,
  "skills": 22,
  "resourcefulness": 15,
  "tags": ["amazon", "divine", "flight", "warrior"]
}
```

#### **Darkseid**
```json
{
  "power": 25,
  "reflexes": 20,
  "movement": 18,
  "resilience": 25,
  "armor": 5,
  "skills": 22,
  "resourcefulness": 25,
  "tags": ["new_god", "cosmic", "omega_beams"]
}
```

### A-TIER (City Level)

#### **Batman**
```json
{
  "power": 6,
  "reflexes": 12,
  "movement": 5,
  "resilience": 5,
  "armor": 10,
  "skills": 25,
  "resourcefulness": 25,
  "tags": ["human", "bat_family", "tech_based"]
}
```

#### **Deathstroke**
```json
{
  "power": 8,
  "reflexes": 16,
  "movement": 10,
  "resilience": 10,
  "armor": 10,
  "skills": 25,
  "resourcefulness": 22,
  "tags": ["enhanced", "mercenary", "healing_factor"]
}
```

### B-TIER (Street Level)

#### **Green Arrow**
```json
{
  "power": 5,
  "reflexes": 12,
  "movement": 5,
  "resilience": 4,
  "armor": 4,
  "skills": 20,
  "resourcefulness": 18,
  "tags": ["human", "archer", "billionaire"]
}
```

#### **Nightwing**
```json
{
  "power": 5,
  "reflexes": 12,
  "movement": 6,
  "resilience": 4,
  "armor": 6,
  "skills": 20,
  "resourcefulness": 15,
  "tags": ["human", "bat_family", "acrobat"]
}
```

***

## AUTO-POPULATION RULES

### For Known Characters (VIP List)
Use hardcoded values above for accuracy.

### For Generic Heroes (Tier 8-15)
**Default Template**:
```json
{
  "power": 12,
  "reflexes": 10,
  "movement": 10,
  "resilience": 10,
  "armor": 2,
  "skills": 8,
  "resourcefulness": 8,
  "tags": ["auto_generic_hero"]
}
```

### For Joke Characters
**Condiment King, Kite Man, etc.**:
```json
{
  "power": 3,
  "reflexes": 3,
  "movement": 3,
  "resilience": 3,
  "armor": 0,
  "skills": 2,
  "resourcefulness": 2,
  "tags": ["joke_tier", "ignore"]
}
```

### For Civilians
**Alfred, Lois Lane, Perry White**:
```json
{
  "power": 1,
  "reflexes": 2,
  "movement": 1,
  "resilience": 1,
  "armor": 0,
  "skills": 5,
  "resourcefulness": 5,
  "tags": ["civilian"]
}
```

### For Cosmic Entities
**Spectre, Anti-Monitor, Presence**:
```json
{
  "power": 25,
  "reflexes": 25,
  "movement": 25,
  "resilience": 25,
  "armor": 0,
  "skills": 25,
  "resourcefulness": 25,
  "tags": ["cosmic", "abstract", "god_tier"]
}
```

***

## SKILLS + RESOURCEFULNESS INFERENCE

### Skills Scoring
```python
if "genius intellect" in bio: skills = 12-15
if "master martial artist" in bio: skills = 18-22
if "expert combatant" in bio: skills = 12-16
if "trained fighter" in bio: skills = 8-12
if "tactical genius" in bio: skills += 5
if "detective" in bio: skills += 3
```

### Resourcefulness Scoring
```python
if "batman" or "wayne" in name: resourcefulness = 25
if "billionaire" in bio: resourcefulness += 10
if "prep time" mentioned: resourcefulness += 5
if "utility belt" or "gadgets": resourcefulness += 8
if "justice league" member: resourcefulness += 5
if "leader" role: resourcefulness += 4
if "loner" or "rogue": resourcefulness -= 3
```

***

## TAG ASSIGNMENT RULES

### Physiologies
```
Kryptonian: immune to normal damage, vulnerable to magic/kryptonite
Atlantean: buffed underwater, debuffed on land
Speedster: time manipulation resistance
Human: baseline vulnerabilities
Martian: psychic powers, fire vulnerability
Divine: magic resistance, divine energy
Demon: holy vulnerability
Robot: EMP vulnerable, no biological needs
```

### Specializations
```
bat_family: night vision, prep immunity
marksman: relies on ranged precision
tech_based: technology dependent
fire_user: buffed by heat, vulnerable to cold
ice_user: buffed by cold, vulnerable to heat
blind: darkness immunity
flight: 3D mobility
```

***

## INTEGRATION WITH GITHUB DATABASE

Your current file `vs_battles_populated.json` needs updating to this format:

```json
[
  {
    "id": 70,
    "name": "Batman",
    "slug": "70-batman",
    "publisher": "DC Comics",
    "alignment": "good",
    "combat_stats": {
      "reflexes": 12,
      "movement": 5,
      "power": 6,
      "resilience": 5,
      "armor": 10,
      "total_offense": 23,
      "total_defense": 15
    },
    "dc_mitigation": {
      "skills": 25,
      "resourcefulness": 25,
      "total_mitigation": 50
    },
    "tags": ["human", "bat_family", "tech_based"],
    "vs_battles_reference": {
      "tier": "9-A",
      "speed": "Peak Human to Subsonic",
      "url": "https://vsbattles.fandom.com/wiki/Batman_(Post-Crisis)"
    }
  }
]
```

***

## NEXT STEPS

1. **Update existing database** with VIP stats
2. **Auto-populate remaining 600+ heroes** using templates
3. **Manual review** of top 50 most important characters
4. **Tag all characters** for threat database compatibility

***

## NOTES

- **Tiers are fluid**: Superman varies from 5-B to 2-C depending on writer
- **Skills + Resourcefulness**: Batman's 50 total mitigation is WHY he can fight Superman
- **Movement cap**: Ground-based heroes max at 5-8 movement regardless of reflexes
- **Generic heroes**: Use tier 12 default - strong enough to matter, weak enough not to break game
- **Joke characters**: Tag as "ignore" for easy filtering