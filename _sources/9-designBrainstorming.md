# Tipping Point Design Brainstorming

## Problem Statememt
The challeneg of Tipping Point is to score Rings on Mobile Goals and move them to our platform to score more points than the opposing Alliance at the end of the match.

## Design Statement
Design, build, test, and compete with a Robot capable of efficiently *scoring Rings* and *manipulating Mobile Goals* in Tipping Point.

## Constraints
- The Robot must not exceed 18" by 18" by 18" before the match starts
- The Robot must be completed by October.
- There is a limit of eight (8) V5 motors per Robot.
- We will need multiple Autonomous Programs since the Autonomous of our Alliance partner will be difficult to predict.

## Robot Criteria
- Must be capable of *Scoring Rings* and *manipulating Mobile Goals*.
- Must be capable of holding multiple *Mobile Goals* at once.

## Robot Componets
- Drive Base; must be fast and resistant to pushing
- Ring or Ringless Design; must be fast, and efficient at its goal.
- Goal is either to score rings on goals __OR__ to just manipulate Mobile Goals.
- Intakes; must be able to grab *Rings* in any position i.e. versatile.
- Mobile Goal Lift; must be able to efficiently grab, hold, and drop Mobile Goals.

## Drive Base Designs
```{figure} ././_images/9/x-drive.png
---
width: 300px
name: x-drive.png
---
X-Drive
```

```{figure} ././_images/9/mecanumDriveBase.png
---
width: 300px
name: mecanumDriveBase.png
---
Mecanum Drive
```

```{figure} ././_images/9/omniDriveBase.png
---
width: 300px
name: omniDriveBase.png
---
Omni Drive
```
## Lift Designs

```{figure} ././_images/9/4bar.png
---
width: 300px
name: 4bar.png
---
Four Bar (4bar)
```

```{figure} ././_images/9/DR4B.png
---
width: 300px
name: DR4B.png
---
Double Reverse Four Bar (DR4B) 
```

```{figure} ././_images/9/6_bar_lift.png
---
width: 300px
name: 6_bar_lift.png
---
Six bar (6bar)
```
### Intake Designs
#### Flaps
#### Flex Wheel


## Lift/Tray Design Matrix
| Design       | Stability | Extension | Speed | Complexity | Total |
|--------------|-----------|-----------|-------|------------|-------|
| 6 Bar        | 2         | 2         | 2     | 3          | 9     |
| 4 Bar        | 3         | 3         | 1     | 4          | 11    |
| DR4B         | 4         | 4         | 3     | 1          | 12    |

Based on our design matrix for Lifts/Trays, the DR4B scored the highest however, we are going with the close second 4 Bar because we do not need as much height as the DR4B gives.

## Robot Archetypes Matrix
| Design    | Mobile Goal Capacity | Complexity | Versatility | Total |
|-----------|---------------|------------|-------------|-------|
| Ring      | 2             | 3          | 4           | 9     |
| Lift      | 3             | 2          | 5           | 10     |
| Ring + Lift| 3            | 5          | 1           | 9     |

Based on our design matrix for Robot Archetypes, the Lift archetype scored highest. Our first robot will be a Lift because of its score as well as the October deadline.

## Intake Design Matrix
| Design | Complexity | Traction | Total |
|--------|------------|----------|-------|
| Flaps  | 1          | 1        |2      |
| Flex Wheels | 1          | 2        |3      |

Based on our design matrix, the Flex Wheels intake scored highest. While we design our Ring + Lift robot we will initally design with Flex wheels since they offer better traction then their flap counterpart.

## Drive Base Matrix
| Design          | Traction | Strafing | Stability | Complexity | Speed | Resistance to Pushing | Total |
|-----------------|----------|----------|-----------|------------|-------|-----------------------|-------|
| Mecanum         | 2        | 2        | 2         | 1          | 2     | 0                     | 9     |
| Omni            | 1        | 0        | 3         | 2          | 2     | 2                     | 10    |
| Omni + Traction | 3        | 0        | 0         | 3          | 0     | 3                     | 9     |
| X-drive         | 0        | 3        | 1         | 0          | 3     | 1                     | 6     |

Based on our design matrix, omni wheels are the best overall, so we will be designing a 4 wheel Omni drive base.

> For the design marticies, higher values are better. Simple designs score higher on the complexity category for this reason.

```{important}
Last Edited on 8/31/21.
```