# Git Status

This document is to provide various commands for checking on the status and state of your repository (local, remote, branches, etc)

## General status about the current state of your directory

`git status`

## Where is `HEAD` pointing?

`git log -1`

## How many commits past the parent branch is my branch?

`NUMCOMMITS=$(git rev-list --count HEAD ^master); echo $NUMCOMMITS`

## What remote branches are available?

`git branch -r`
