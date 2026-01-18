# Speaker and Talk registry for Python Australia

This repository contains a registry of people, and their talks, that have been presented at Python community events in
Australia alongside several scripts to retrieve information about speakers and their speeches.

## Data Model

There are two registries that should be edited, ``Speaker`` and ``Talk``. The registries follow the below data
models, however additional, arbitrary, data may be added as appropriate. The ``name`` field in the Speaker registry
should correspond to the ``speaker`` field in the Talk registry. More explicitly these two fields will be used to
"join" the two registries.

### Speaker Registry

Each speaker is represented as a table in the ``data/speaker_registry.toml`` file. The data model for the speaker
registry is as follows (using Kai as an example):

```toml
[KaiStriega]  # This is an arbitrary, but unique, identifier
name = "Kai Striega"
pronouns = "he/him"
about = "Kai is a motivated, conscientious senior software developer and FOSS advocate with an educational background in mathematics. Whilst being very appreciate the beauty of Mathematics Kai prides himself on his ability to focus on pragmatic outcomes, prioritising his work effectively. This combined with his strong technical grounding have seen him succeed in his roles as a software developer and data engineer at BHP, and now as a senior software engineer at Cartesian Software. In addition to his professional work, Kai is active in the Free and Open Source community as a long-term maintainer of SciPy."
city = "Sydney"
socials = { "LinkedIn" = "https://www.linkedin.com/in/kai-striega/", "GitHub" = "https://github.com/Kai-Striega" }
```

### Talk Registry

Each talk is represented as a table in the ``data/talk_registry.toml`` file. The data model for the talk registry is as
follows:

```toml
[KaiMcDonalds]  # This is an arbitrary, but unique, identifier
speaker = "Kai Striega"
title = "Optimising Your McDonald's Order: An Introduction to Linear and Mixed Integer Programming with Pyomo"
length_in_mintues = 30
abstract = """
Ever wondered if you could hack your McDonald's order to be as low-calorie as possible while still meeting all your
essential dietary needs? In this talk, we’ll dive into Linear Programming (LP) and Mixed Integer Programming (MIP)
using Pyomo, a powerful Python library for optimisation. We’ll start with the basics—what LP and MIP are, why they’re
useful, and how they help solve real-world problems. We’ll then put theory into practice by setting up an optimisation
problem: finding the lowest-calorie McDonald’s meal that still meets all your nutritional requirements. Using Pyomo,
we’ll model the problem, define constraints, and let an optimisation solver do the heavy lifting.
By the end of the session, you’ll have a solid understanding of how LP/MIP works, see how to apply it in Python, and
walk away with a fun (and possibly surprising) take on fast-food decision-making!
"""
presented_at = "PythonWA"
presentation_date = 2025-04-03
```
