# Golf Card Game Scorekeeper

A simple web app for tracking scores in the Golf card game (6-card variant).

## Usage

Open `index.html` in any web browser. No server or build tools required.

## Features

- **2-8 players** with custom names
- **9-round scoring** with easy input
- **Quick score panel** for fast entry on mobile
- **Automatic totals** with winner highlighting
- **Persists across refreshes** via localStorage
- **Keyboard navigation** (arrow keys, Tab, Enter)

## Golf Card Game Scoring

| Card | Points |
|------|--------|
| Joker | -2 |
| 2 | -2 |
| Ace | 1 |
| 3-10 | Face value |
| Jack, Queen | 10 |
| King | 0 |
| Matching pair (column) | 0 |

Lowest score wins.
