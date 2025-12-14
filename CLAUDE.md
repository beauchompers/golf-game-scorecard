# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Golf Card Game Scorekeeper - a single-page web app for tracking scores in the Golf card game (6-card variant). No build tools or dependencies; open `index.html` directly in a browser.

## Architecture

Single file (`index.html`) containing:
- **CSS** (lines 7-385): Embedded styles with responsive design, golf-green theme
- **HTML** (lines 387-488): Setup screen, game screen, and quick-score panel
- **JavaScript** (lines 490-844): Vanilla JS with global `gameState` object

### Key State Management
- `gameState` object holds all game data: `players[]`, `scores[][]` (playerIndex × holeIndex), `numPlayers`, `started`
- State persists to `localStorage` under key `golfCardGame`
- `scores[playerIndex][holeIndex]` uses `null` for empty, integers for entered values

### Screen Flow
1. **Setup Screen** (`#setup-screen`): Player count selection (2-8), name inputs
2. **Game Screen** (`#game-screen`): Score table with inputs, totals, winner highlighting
3. **Quick Score Panel** (`#quick-score`): Fixed bottom panel for fast score entry

### Core Functions
- `init()` → `loadGameState()` → `showSetupScreen()` or `showGameScreen()`
- `renderScoreTable()`: Rebuilds entire table HTML, attaches event listeners
- `handleScoreChange()`: Updates state, saves, re-renders
- `saveGameState()`/`loadGameState()`: localStorage persistence
