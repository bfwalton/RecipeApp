---
layout: landing
permalink: /import-recipes/
title: Import
heading: Bring the recipes you already have
eyebrow: Importing
seo_title: "Import Recipes to iPhone — Paprika and .sauce Files"
description: "Import your recipes into Saucier. It reads Paprika's .paprikarecipes export directly, and tells you exactly what will and won't come across first."
lead: >-
  Years of saved recipes are the reason most people stay in an app they have
  stopped enjoying. Moving them should take one file and five minutes.
cta_heading: Bring them over.
cta_body: >-
  Export from your old app, open the file in Saucier, review what came across.
  Nothing is added to your library until you say so.
howto_name: How to import your recipes into Saucier
howto:
  - title: Export from your current app
    text: >-
      In Paprika, use its export option to produce a .paprikarecipes file. Save
      it to Files, AirDrop it to your iPhone, or email it to yourself.
  - title: Open the file on your iPhone
    text: >-
      Tap the file and choose Saucier, or open Saucier and use Import from the
      settings screen. Saucier identifies the format by reading the file rather
      than by trusting its extension.
  - title: Review what came across
    text: >-
      Saucier shows you every recipe it found, and tells you up front which
      fields it has nowhere to put, before anything is added.
  - title: Import
    text: >-
      Confirm, and the recipes join your library and sync to your other devices
      over iCloud.
faq:
  - q: Which files can Saucier import?
    a: >-
      Paprika's `.paprikarecipes` and `.paprikarecipe` exports, and Saucier's own
      `.sauce` files. Saucier works out which it has by inspecting the contents,
      not the file extension — which matters, because a single recipe exported
      from Paprika often arrives with no extension at all.
  - q: What comes across from Paprika?
    a: >-
      The name, ingredients, directions, your notes, Paprika's own description,
      the source and source link, the photo, servings, nutrition, prep, cook and
      total times, and categories. The first category becomes the recipe's
      folder in Saucier and the rest are shown to you during the review.
  - q: What does not come across?
    a: >-
      Star ratings and difficulty. Saucier has nowhere to put them, so rather
      than silently dropping them it lists them during the review — finding out
      months later that your ratings stayed behind is not a good way to find out.
  - q: Will importing create duplicates?
    a: >-
      Imports are reviewed before anything is written, so you see the full list
      and decide. Nothing is added to your library until you confirm.
  - q: Can I get my recipes back out of Saucier?
    a: >-
      Yes. Export your library as a `.sauce` file at any time from settings, and
      share individual recipes as files or links. Your recipes are also stored
      in your own iCloud account rather than on a Saucier server.
  - q: I use a different app — can I still move over?
    a: >-
      Not as a single file yet; Paprika and Saucier's own format are what the
      importer reads today. In the meantime, most apps can share a recipe's
      original web link, and Saucier can save from that. If there is a format
      you need, say so at help@saucier-app.com — it is useful to know what
      people are actually trying to move.
screenshot: /assets/img/screens/import.jpg
screenshot_alt: "Saucier's Import Recipes screen with a button to choose a recipe file."
---

Switching recipe apps is not really about features. It is about the two hundred
recipes you have already saved, and whether you are willing to lose them. For
most people the answer is no, which is why so many people stay put.

So Saucier reads other apps' files, and tells you the truth about what it can
and cannot carry.

## From Paprika

Export your library from Paprika as a `.paprikarecipes` file, then open it on
your iPhone — tap it in Files and pick Saucier, or use **Import** inside
Saucier's settings.

Saucier handles all three shapes of Paprika export that turn up in practice: the
usual zipped-and-gzipped archive, archives whose entries were written as plain
JSON, and a single recipe exported as a bare gzip with no archive around it. It
works out which one it has by looking at the bytes, because the extension is the
same for the first two and frequently missing on the third.

### What comes across

| From Paprika | Into Saucier |
|---|---|
| Name | Recipe name |
| Ingredients | Ingredients, re-parsed so amounts can be scaled and converted |
| Directions | Method, split into steps |
| Notes and description | Notes, yours first |
| Source and source URL | Author and original link |
| Photo | Recipe photo |
| Servings | Servings |
| Nutritional info | Nutrition |
| Prep, cook and total time | Prep, cook and total time |
| Categories | The first becomes the folder; the rest are shown during review |

### What does not

**Star ratings** and **difficulty**. Saucier has nowhere to put either, so
instead of dropping them quietly it lists them for each recipe during the
review step. You find out before you import, not six months later.

## From Saucier

Saucier's own `.sauce` files work in both directions. Export your whole library
from settings as a backup, or share a single recipe as a file to someone else
who uses the app. Older `.sauce` files still open — the format has stayed
backward-compatible across every version.

## Nothing happens until you say so

The import screen is a review, not a progress bar. You see every recipe the file
contained and every field that has no home, and the library is only written when
you confirm. An import that silently half-worked is worse than one that did not
run.

## And getting back out

Your recipes are stored on your device and synced through your own iCloud
account — not on a Saucier server, because there isn't one. You can export the
whole library to a `.sauce` file whenever you like, and share any single recipe
as a file or a link.

Being easy to leave is a feature. It is the reason you are reading this page
about leaving something else.

## Starting from scratch instead?

If your recipes are not in another app but scattered across saved posts and open
tabs, that is the other half of the problem:
[saving from Instagram, TikTok and the web →]({{ '/save-recipes-from-instagram-tiktok/' | relative_url }})
