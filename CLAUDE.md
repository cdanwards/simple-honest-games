# Project Instructions

## Who This Is For

This project is designed for young kids (ages 4-6) learning to read, type, and use a computer. All content must be age-appropriate, encouraging, and fun. Games should never punish mistakes -- just encourage trying again. The site is published as "Simple Honest Games" at simplehonestgames.kids.

## Architecture

- Each game is a single self-contained `.html` file (no external dependencies)
- `index.html` is the hub page linking all games
- Zero build tools, zero frameworks -- just open in a browser

## Design System

All games must use these consistent styles:

### Colors
- Background: `#fef3c7` (warm yellow)
- Primary: `#7c3aed` (purple)
- Title text-shadow: `2px 2px 0 #fbbf24` (gold)
- Card borders: `#93c5fd` (light blue)
- Success: `#34d399` / `#059669` (green)
- Error: `#fca5a5` / `#dc2626` (red, gentle)
- Text: `#4b5563` (gray)
- Muted: `#9ca3af` (light gray)

### Typography
- Font: `'Comic Sans MS', 'Chalkboard SE', cursive`
- Title: 3rem, purple with gold text-shadow
- Subtitle: 1.5rem, gray

### Common UI Elements
- **Mode toggle**: Top-right corner, pill buttons with `border: 3px solid #c4b5fd`, active state uses purple fill
- **Back link**: Top-left corner, `<a href="index.html" class="back-link">` styled as a pill
- **Score bar**: Pill-shaped white spans with `box-shadow: 0 2px 10px rgba(0,0,0,0.08)`
- **Cards/displays**: White background, `border-radius: 30px`, `border: 6px solid #93c5fd`
- **Confetti**: Emoji particles with CSS `fall` animation, spawned via JS
- **Celebration messages**: Array of encouraging phrases with emojis, randomly picked
- **Try again messages**: Gentle encouragement, never discouraging

### Animations
- `celebrate`: scale + rotate bounce (for correct answers)
- `shake`: translateX wiggle (for wrong answers)
- `pop`: quick scale bounce (for filling in slots)
- `fall`: translateY + rotate (for confetti)
- `pulse`: box-shadow breathing (for active elements)

## Adding a New Game

1. Create `new-game.html` as a single self-contained file
2. Copy the design system styles (background, fonts, colors, mode toggle, back link, confetti)
3. Include the back link: `<a href="index.html" class="back-link">🏠 Home</a>` with matching CSS
4. Include mobile-responsive media queries (`@media (max-width: 600px)`) and touch support
5. For keyboard-input games, add an on-screen mobile keyboard
6. Add the game card to `index.html`:
   - Choose an accent color (blue, green, purple, orange, pink, or add a new one)
   - Add `<a href="new-game.html" class="game-card {color}">` with icon, name, and description
7. Include score/streak tracking and celebration messages for consistency
8. Test in browser at both desktop and mobile widths (~375px)

## Existing Games

| File | Game | Description |
|------|------|-------------|
| `index.html` | Hub Page | Central navigation with game cards |
| `letter-match.html` | Letter Match | Type the displayed letter (upper/lower/mixed modes) |
| `word-speller.html` | Word Speller | Spell emoji words letter by letter (easy/medium/hard) |
| `memory-match.html` | Memory Match | Flip cards to find emoji pairs (4x4 / 5x4 / 6x6) |
| `letter-tracing.html` | Letter Tracing | Trace letters/numbers with mouse/touch (easy/medium/hard) |
| `story-builder.html` | Story Builder | Pick character + activity + location, get a story |
| `number-bonds.html` | Number Bonds | Find the missing number in addition pairs (to 5/10/20) |
| `sight-words.html` | Sight Words | Read and type sight words from memory (pre-K/kinder/1st) |

## Hub Page Accent Colors

| Color | Border | Hover | Name Color |
|-------|--------|-------|------------|
| blue | `#93c5fd` | `#3b82f6` | `#2563eb` |
| green | `#86efac` | `#22c55e` | `#16a34a` |
| purple | `#c4b5fd` | `#7c3aed` | `#7c3aed` |
| orange | `#fed7aa` | `#f97316` | `#ea580c` |
| pink | `#fbcfe8` | `#ec4899` | `#db2777` |
| teal | `#99f6e4` | `#14b8a6` | `#0d9488` |
