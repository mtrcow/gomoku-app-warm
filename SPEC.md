# Gomoku App - 暖色舒適風格 SPEC.md

基於 Notion / Claude 暖色美學嘅五子棋遊戲

---

## 1. Concept & Vision

一款以暖色、木質氛圍為基礎的五子棋遊戲。配色靈感來自咖啡館、木紋桌面、秋天樹葉。令人感到舒適、放鬆，適合悠閒地與朋友下棋。唔係冷冰冰嘅科技產品，而係一杯暖嘅朱古力。

---

## 2. Design Language

### 2.1 Visual Theme
- **風格**：暖色舒適美學 — 木質色調、柔和光澤、咖啡廳氛圍
- **情緒**：溫暖、舒適、悠閒
- **參考**：Notion、Codepen warm UI、Coffee shop aesthetic

### 2.2 Color Palette

| Role | Color | Hex |
|------|-------|-----|
| Background (Primary) | Warm Cream | `#FDF6E9` |
| Surface | Soft White | `#FFFCF7` |
| Board | Wooden Brown | `#C4956A` |
| Grid Lines | Dark Wood | `#8B6914` |
| Black Piece | Rich Espresso | `#2C1810` |
| White Piece | Cream White | `#FFF8E7` (with shadow) |
| Accent | Terracotta | `#E07A5F` |
| Text Primary | Dark Brown | `#3D2914` |
| Text Secondary | Warm Gray | `#9A8B7A` |
| Winner Highlight | Golden Amber | `#F4A261` |

### 2.3 Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| Title | Georgia, serif | 600 | 28px |
| Heading | Georgia, serif | 500 | 20px |
| Body | System-ui | 400 | 16px |
| Caption | System-ui | 400 | 13px |
| Button | System-ui | 500 | 15px |

*Fallback: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif*

### 2.4 Spacing System

- Base unit: **8px**
- Board padding: **48px** (6 units)
- Piece size: 38px diameter (cell 44px, 3px margin)
- Grid cell: 44px × 44px
- Button padding: 12px 24px

### 2.5 Motion Philosophy

- **Ease curve**: `ease-out` — 柔和自然
- **Duration**: 200ms (micro), 350ms (standard)
- **Piece placement**: Scale from 0.7 → 1.0 with gentle bounce
- **Win detection**: Gentle warm glow pulse
- **No jarring transitions**

### 2.6 Depth & Elevation

- Board: warm wood texture effect with subtle shadow
- Pieces: 3D effect with inner highlight for white piece
- Buttons: rounded, soft shadows

---

## 3. Layout & Structure

```
┌─────────────────────────────────────┐
│           Header (Title)             │  Warm Brown text
├─────────────────────────────────────┤
│         Status / Turn Info          │  Terracotta accent
├─────────────────────────────────────┤
│                                     │
│           Game Board                │  Wooden brown
│          (15×15 grid)               │  Warm shadows
│                                     │
├─────────────────────────────────────┤
│         Action Buttons              │  Terracotta buttons
│    [New Game]  [Undo]               │
└─────────────────────────────────────┘
```

---

## 4. Features & Interactions

### 4.1 Core Features

- 15×15 standard board
- Click intersection to place pieces
- Alternating black/white, black goes first
- Real-time win detection (horizontal/vertical/diagonal)
- Winning pieces glow with warm amber

### 4.2 Interaction Details

| Action | Visual Feedback |
|--------|-----------------|
| Hover cell | Subtle warm highlight |
| Click cell | Piece appears with bounce animation |
| Win | Winning pieces pulse warm amber |
| New Game | Board fades and resets |

---

## 5. Technical Approach

### 5.1 Stack
- Single HTML file with embedded CSS and JavaScript
- No dependencies, pure vanilla

### 5.2 Output
`/Users/tonyopenclaw/.openclaw/workspace-chuxuan/projects/gomoku-app-warm/index.html`

---

## 6. Acceptance Criteria

- [ ] Warm cream background
- [ ] Wooden brown board
- [ ] Black pieces clearly visible (espresso brown)
- [ ] White pieces clearly visible (cream with dark border)
- [ ] Terracotta accent buttons
- [ ] Warm glow on win
- [ ] Smooth animations
- [ ] Mobile responsive
