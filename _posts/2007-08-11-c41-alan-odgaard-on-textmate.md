---
title: 'C4-[1]: Alan Odgaard on TextMate'
date: 2007-08-11 00:00:00 Z
layout: post
---

Alan Odgaard is the Danish developer behind TextMate, an elegant and hugely customizable editor favored by programmers on the Mac. I spend most of my day in TextMate, so it’s great to take a peek behind the scenes.

TextMate was born out of Alan’s dissatisfaction with Xcode; he had several other projects in the works, but none of them really grabbed his attention. Early versions of TextMate got spillover buzz from the original Rails screencast, which pushed him to get to 1.0 quickly. His priorities didn’t necessarily match the community’s; for example, print support was missing in 1.0. Features like snippets, tab triggers, folding, and columnar editing are some of TextMate’s big sells. More generally, the editor’s overall embrace of customization has been a huge sell.

The customization model starts with input (key strokes, dropped files, tab triggers) and context (file type, project type, location in file, SCM, editor state). Actions like inserting text and running commands can then be performed. The more context available, the more the available actions can be tailored to the task at hand.

Alan thinks his model can be generalized to other applications. Breaking out contexts into *declarative semantic abstractions*, in Alan’s estimation, makes working easier and more foolproof for users. He claims to not work particularly hard on TextMate’s community aspect; its bundles feature makes sharing customizations easy. In the near future, bundles will be moved to a distributed version control system (they currently live in a central Subversion repository). Bundles will be visible to the user as a set of features to be flipped on and off.
