# the-cost-of-a-call

## Overview

Replay review is intended to correct officiating errors—especially in moments that can determine the outcome of a game. But anyone who watches the NFL knows that some of the most controversial calls still stand, even after multiple camera angles and slow-motion replays.

This project examines **how replay review decisions behave in high-leverage situations**, with a focus on consistency, risk, and impact. Rather than analysing a single game or call, the goal is to understand replay review as a *decision system operating under pressure*.

Using NFL play-by-play data from multiple seasons, this analysis asks:
- When are replay reviews most likely to occur?
- Are high-stakes moments treated differently?
- Which types of plays are hardest to overturn?
- How costly are replay decisions when they are wrong?

---

## Key Questions

This project is structured around four core questions:

1. **Where do replay reviews happen?**  
   Are reviews concentrated in close games, late situations, or high-impact moments?

2. **Does leverage change replay behaviour?**  
   Are officials more or less likely to overturn calls when the stakes are highest?

3. **Which play types are most controversial?**  
   Do passes, runs, special teams plays, or turnovers behave differently under review?

4. **What is the cost of a decision?**  
   How much do replay rulings shift win probability when they stand or are overturned?

---

## Data

- **Source:** Public NFL play-by-play data (2009–2018)  
- **Scope:** Only plays involving a replay review or a coach’s challenge  
- **Metrics used:**  
  - Win Probability (WP)  
  - Win Probability Added (WPA)  
  - Game context (score differential, quarter, time remaining)  

To keep the analysis focused and transparent, only columns directly relevant to replay review and leverage were used.

---

## Methodology (High-Level)

- Replay reviews were identified using official replay/challenge flags.
- **High-leverage plays** were defined using pre-committed criteria:
  - Large swings in win probability (|WPA| ≥ 0.15)
  - Late fourth-quarter situations
  - One-score games
- Plays were grouped by:
  - Leverage level
  - Play type
  - Turnover vs non-turnover context
- Results were summarised using overturn rates and win probability impact.

Importantly, this analysis does **not** make claims about intent or officiating bias. It focuses on *patterns* and *consequences*, not blame.

---

## Key Findings

- **Replay reviews overwhelmingly occur in high-leverage moments**, confirming that the system is used when decisions matter most.
- **Overturn rates remain nearly identical regardless of leverage**, suggesting replay review applies a consistent standard even in high-pressure situations.
- **Turnover-related plays stand out sharply**:
  - They carry more than **three times the median win probability impact** of non-turnover plays.
  - Yet they are **far less likely to be overturned**.
- **Passing plays dominate replay reviews**, reflecting the complexity of possession and control rules.
- **Special teams plays**, though rare, tend to be extremely high-impact when reviewed.

Together, these results suggest that replay review struggles most where decisions are both *important* and *visually ambiguous*—especially on possession-changing plays.

---

## Interpretation

Replay review is consistent, but consistency does not guarantee correctness.

The system applies similar overturn standards regardless of how important a play is. As a result, when a mistake occurs in a high-impact moment—particularly on a turnover—it is more likely to stand, even though the consequences are much larger.

This helps explain why certain calls feel uniquely frustrating to fans: not because they happen often, but because when they do happen, replay is least equipped to fix them.

---

## Limitations & Extensions

- This analysis does not evaluate whether individual calls were “right” or “wrong.”
- No video or tracking data was used—only play-by-play outcomes.
- Replay outcomes are treated as final decisions, not ground truth.

Potential extensions include:
- Incorporating tracking or player-position data
- Studying replay outcomes by the officiating crew
- Comparing regular season vs playoff behaviour
- Analysing public disagreement with replay outcomes

---

## Why This Project

This project was inspired by a high-profile, late-game turnover ruling that stood after review and ultimately decided a playoff game. Rather than focusing on that single moment, this analysis asks a broader question: **Are those moments outliers, or symptoms of a deeper pattern?**

The findings suggest the latter.

---

## Tools Used

- Python (pandas, numpy, matplotlib)
- NFL play-by-play data

---

## Final Takeaway

Turnovers, especially fumbles, are some of the most important plays in football. They can completely flip a game. But they’re also some of the hardest calls to get right. Was the player down? Did he actually control the ball? Did it move when it hit the ground?

The data shows that these turnover plays are less likely to be overturned, even though they matter the most. Not because refs don’t care, but because replay needs clear evidence, and fumbles rarely give you a clean camera angle.

So what ends up happening is this: The biggest, messiest plays are the ones that replay is least able to fix. And when one of those goes the wrong way late in a game, it sticks, even if everyone watching at home feels like the call was wrong.

That’s why plays like controversial fumbles feel so brutal. It’s not just bad luck or bias. It’s a replay system that works fine most of the time, but struggles exactly when football gets chaotic and emotional

