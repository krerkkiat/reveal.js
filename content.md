# Reinforcement Learning

March 2, 2024

---

## Introduction

<!-- .slide: data-ou-bg-type="light" -->

- Approach
- Implementation
- Results
- Summary and Discussion
- Q&A

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

## Summary and Discussion

---

## Q&A
