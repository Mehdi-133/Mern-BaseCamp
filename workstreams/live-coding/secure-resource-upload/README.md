# 💻 Secure Real Resource Upload — Live Coding

> **Activity:** Live Coding — `Upload réel sécurisé : fichier, ressource MongoDB et accès contrôlé`
>
> **YouCode ID:** `#82567`

## 📅 Confirmed activity record

| Detail | Confirmed information |
| --- | --- |
| Date and time | Tuesday, 13 October 2026 at 14:30 |
| Duration | Not specified |
| Work mode | Listed as `en binôme` |
| Board participants | Chahd Mazouz and Mouncif Benhar |
| Assigned by | Mehdi LARAIBI |
| Board state on 19 October | `Finished` |

## 🎯 Scenario connection

This activity title matches the Brief 2 implementation flow now present in the LMS source:

1. receive one multipart file with Multer;
2. constrain type and size;
3. store it using a generated name;
4. create a module-linked MongoDB resource;
5. enforce authenticated, role-based, and ownership access;
6. remove partial storage when later work fails.

## 🗂️ Workspace

| Area | Purpose | Status |
| --- | --- | --- |
| [Concepts](./concepts/) | Reuse the Brief 2 Multer lesson | 🟡 Reference prepared |
| [Notes](./notes/) | Source and evidence boundaries | ✅ Recorded |
| [Exercises](./exercises/) | Learner-owned planning exercise | ⬜ Not started |
| [Reviews](./reviews/) | Future attempt and runtime feedback | ⬜ No attempt saved |

## ⚠️ Evidence boundary

- The board proves the class activity is marked `Finished`; it does not show Mehdi as a participant.
- No original live-coding attempt or mentor review was collected.
- The LMS source is separate evidence: basic upload is merged, later ownership/signature hardening is branch-only, and runtime upload tests remain unverified.

## 🚀 One next action

Before looking at the LMS code, write the middleware and controller responsibilities as six ordered comments in the [exercise](./exercises/).

**Observable check:** the comments put authentication and authorization before storage and put MongoDB metadata creation after file validation.
