# Reinforcement Learning

March 2, 2024

---

## Agenda

<!-- .slide: data-ou-bg-type="light" -->

- Background
- Approach
- Implementation
- Results
- Discussion
- Summary
- Q&A

---

## Introduction

Reinforcement learning see an increasing success in various application domains.
One recent sucess is the winning of an RL-based bot developed by Goodfriend [@goodfriend2024competition](#/references).

This bot won the 2023 IEE CoG MicroRTS competition [@richoux2020microphantom](#/references).

---

## Introduction

MicroRTS is a real-time strategy game created by Santiago [@ontanon2013combinatorial](#/references) in 2013.
It is a simplified version of a real-time strategy game aiming for fast ideal validation
in research.

---

## Approach

<!-- .slide: data-ou-bg-type="light" -->

---

## Implementation

----

## Data Preparation

```py
import pandas as pd
from tabulate import tabulate

df = pd.DataFrame(data=data)
df["Total"] = df.sum(axis=1)
df = df.transpose()

format = "github"
print(
    tabulate(
        df,
        tablefmt=format,
        headers=["1", "2", "3", "4", "5"],
        floatfmt=".4f",
    )
)
```

----

## Experiment Design

---

## Results

---

## Discussion

---

## Summary

---

## Q&A
