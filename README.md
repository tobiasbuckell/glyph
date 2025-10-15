# Glyph: Keyboard-first editing for authors/non-programmer writers

[![image](https://github.com/tobiasbuckell/glyph/blob/main/glyph-keyboard-layer.jpg)](https://github.com/tobiasbuckell/glyph/blob/main/glyph-keyboard-layer.jpg)

A Karabiner-Elements layer that gives you some vim-flavored navigation anywhere in OS-X. It also has a press-and-hold **select** mode for easy text selection. To use: copy the text in JSON files Glyph 1, Glyph 2, Glyph 3, and Glyph 4 that are posted here one at a time, and then paste them into Karabiner by going to Settings --> Complex Modifications --> 'add your own rules' and pasting them into the pop-up. Once enabled, hit capslock to move around and then capslock to leave the navigation. "Glyph Mode activated!" should appear in the lower right of your screen if it triggers.

This was inspired **heavily** by the hard work done by **karabiner-vim-mode-plus** (if you want vim system-wide on your OS-X environment, go here for Vim Mode Plus: [GitHub](https://github.com/jonasdiemer/karabiner-vim-mode-plus))

## 1) What you get with Glyph:
- **Navigation layer**: hit 'capslock' and IJKL moves your around and it works system-wide.
- **Hold-to-select**: hold `d` to select as you move (think of it as the DEFINE key)
- **Cut/Paste** helpers: `s` = SCOOP (cut), `f` = FILL (paste).
- **Paragraph/line smart jumps** for writers.
- **Hit capslock or escape again** to go back to your normal keyboard typing.

## 2) Modes

### 2.1 Glyph Mode (navigation layer)
Glyph Mode is activated by tapping "capslock." When active:
- **Move normally** with the keys listed below.
- **Hold `d`** to 'define' the text and enter Select Mode (adds SHIFT to your moves).
- **Release** `d` to stop selecting, use 's' to 'scoop' up text, or 'f' to fill in text.

### 2.2 Select Mode (hold `d`)
While **holding `d`** (for Define), movement keys include **Shift** so text becomes selected as you move (e.g., ← becomes ⇧←, ⌥↑ becomes ⌥⇧↑, etc.).

## 3) Keymap (Glyph Mode)

> The table shows **the key pressed** when in Glyph mode on the left and what it does normally, and what it does when you hold `d` on the right.

| You press | Action                 | Normal move | Hold `d` (Select) |
| --------- | ---------------------- | ----------- | ----------------- |
| `h`       | **Start of line**      | ⌘←          | ⌘⇧←               |
| `;`       | **End of line**        | ⌘→          | ⌘⇧→               |
| `u`       | **Start of paragraph** | ⌥↑ (×2)     | ⌥⇧↑ (×2)          |
| `o`       | **End of paragraph**   | ⌥↓          | ⌥⇧↓               |
| `m`       | **Left 1 char**        | ←           | ⇧←                |
| `.`       | **Right 1 char**       | →           | ⇧→                |
| `i`       | **Up 1 line**          | ↑           | ⇧↑                |
| `k`       | **Down 1 line**        | ↓           | ⇧↓                |
| `j`       | **Word-left**          | ⌥←          | ⌥⇧←               |
| `l`       | **Word-right**         | ⌥→          | ⌥⇧→               |

### Extra motions available in the block (optional)
In addition you can move or select to the start or end of the whole document:

|Key|Action|Normal|Select|
|---|---|---|---|
|`y`|Start of document|⌘↑|⌘⇧↑|
|`n`|End of document|⌘↓|⌘⇧↓|

## 4) Editing commands
These are simple helpers wired in your block:

| Key | Action             |
| --- | ------------------ |
| `s` | Scoop (cut, or ⌘X) |
| `f` | Fill (paste or ⌘V) |


## 5) Setup & usage

1. **Install Karabiner-Elements** https://karabiner-elements.pqrs.org
2. **Add the JSON** via _Karabiner-Elements → Complex Modifications_ and clickin 'Add your own rule.'
3. **Paste in JSON** from the 4 JSON files here, copy and paste them 4 times using 'add to add 4 rules of your own.
4. **Test**:
    - Tap the direction keys above to move.
    - **Hold `d`** and press movement keys to select.
    - Use `s` to strike (cut), `f` to fill (paste).

## 6) Tips & notes

- **Repeat selection**: holding `d` while holding a movement key will smoothly expand the selection as the key repeats (Karabiner repeats the target key).
- **App conflicts**: if an app already uses these shortcuts, your app may “win.”
- **Word behavior**: macOS jumps to the start of the word, and to the end of the word. As a writer you may want this to jump to the start of the next word. I may even add that by having it jump an extra space after jumping to the end of a word, but there's some weird behavior that can emerge, so for public release I leave it jumping to the end of the word.
- **Paragraph behavior**: macOS defines “paragraph” by blank-line boundaries and some text system rules. If a paragraph jump feels off in certain apps, that’s the app’s text system—not your mapping.
- **Line behavior**: macOS defines 'start of the line' differently than an author and just jumps to the left of the screen. I'm working on how to get it to jump by sentences, but haven't gotten a solution I like.
- **Order of rules**: if you maintain multiple complex modifications, keep your Glyph Mode rules together and (if needed) above app-specific overrides—(for example, I keep my custom Colemak layout at the bottom of the Karabiner Complex Modifications list of rules). Make sure the 'no undefined keys' rule at the bottom of the Glyph rules and above your custom rules.
- **Start small**: just get used to hitting capslock and moving around with your IJKL keys as first, and then move to using the 'd' key to mark text. The Z,X,C,V keys all work the way they do when you hit Apple or CTRL plus Z,X,C,V, so they should be easy to adapt to using to manipulate text.

## 7) Troubleshooting
- **Selection doesn’t happen**: remember selection only occurs when **holding `d`**.
- **Anything else**: No guarantees, I'm releasing this in hope others will find it useful but can't help out much if something goes wrong.

## 8) Why this layout?
- This was inspired by looking at emacs and vim users in other realms and wanting a keyboard-first editing system. For the last ten years I've played with variations of this, but finally decided to create this as a concept and release it out of a desire to let writers know we don't have to use a mouse and kill our wrists when editing, the concept of layers and keyboard editing is solved in programming circles, why not imitate? But I found emacs and vim to not 'fit' with my brain, whereas WASD keys and IJKL keys do. Out of that came a more gestural keyboard layout.
- Additionally, I wanted the visual nature of the keyboard layout to be a little easier to learn. I'm not a coder, I'm ADHD, and the size of the list and concepts needed to memorize vim as I was learning it were daunting and often got in the way and tripped me up while writing. But my gaming instincts for IJKL are hard, hardwired. The moment I mapped IJKL and a leading key to motion, I was off and running.
- Over time I've fiddled a bit, and then came up with holding the 'd' key as a shift key. Combining simple motion with a held down key to select made sense and was quick for muscle memory to adapt to.
- The movement keys also have a hierarchy that I found easier to memorize. Paragraph navigation occurs on the higher row with 'u' and 'o' keys, then word navigation on the home layer with 'j' and 'l' keys, and then you drop down a keyboard row for character navigation with 'm' and '.' You drop your fingers down as you get more defined in what you are moving or selecting (on an ortholinear keyboard this is a *very* smooth motion).
- This is a huge readme, but all you need to do is get the JSON pasted into Karabiner, 4 JSON files that need cut and pasted into 4 'add your own rules' entry areas. Then turn it on and hit capslock to move around, capslock to leave the navigation.
- Why capslock? When was the last time you used it? It's a big, easy to hit key that, unless we're in some specialized industry, we only hit once or twice a year. Doing literally anything else with a capslock key is more useful.

### Credits / Inspiration
- **karabiner-vim-mode-plus** [GitHub](https://github.com/jonasdiemer/karabiner-vim-mode-plus)
- **Hyper IJKL** [Github](https://github.com/RomanYuldashev/HyperIJKL)
