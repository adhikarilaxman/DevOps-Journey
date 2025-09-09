---

# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Git Branching Strategy

A branching strategy is a plan for how developers use branches in Git so that everyone can work together without breaking the main project.

---

### Why use Branches?

1. To try new things without breaking the main code.
2. To fix bugs separately.
3. To organize teamwork.

---

### What is a Branch?

A branch in Git is like a separate copy of the project where you can work without disturbing the main code.

---

## Calculator Example with Git Branching

**Version 1 (v1) – Only Add & Subtract**

* Create a branch `v1`.
* Add code for addition and subtraction only.
* Merge into `main`.

**Version 2 (v2) – Add Multiplication**

* Create a new branch from `main` → `v2`.
* Add multiplication feature.
* Merge into `main`.

**Version 3 (v3) – Add Division**

* Create a branch `v3` from `main`.
* Add division feature.
* Merge back into `main`.

**Hotfix Example**

* Suppose in `v2` multiplication was wrong (e.g., it adds instead of multiplies).
* Create branch `hotfix-multiply`.
* Fix the bug.
* Merge into `main`.

---

## Git Branch Types Explained

**1. Main / Master Branch**

* The main codebase where stable and production-ready code lives.

**2. Feature Branch**

* Used when you want to add a new feature.
* Created from `main`, worked on, tested, and then merged back.

**3. Release Branch**

* Created when preparing a new version for release.
* Only bug fixes and final touches (no new big features).

**4. Hotfix Branch**

* Used when something is broken in production and needs urgent fixing.
* Created directly from `main`, fixed quickly, and merged back.

---

### Summary

* Main/Master → Always working code (production).
* Feature → For new features (temporary branch).
* Release → For preparing a new version.
* Hotfix → For urgent bug fixes.

---

Do you want me to also make a **simple text-based diagram** (branching tree) to include in your notes, so it’s easier to visualize without images?
