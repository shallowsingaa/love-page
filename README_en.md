# Valentine Love Letter Page

A beautiful Valentine's Day love letter webpage with typewriter effect, falling hearts, fireworks, and background music.

## Features

- **Typewriter Effect** — Letter content types out character by character
- **Falling Hearts** — Continuous heart animation falling from the sky
- **Fireworks** — Click the edge of the page or the heart icon to trigger fireworks
- **Background Music** — Play your favorite music on loop
- **Light/Dark Theme** — One-click toggle between themes
- **Responsive Design** — Works perfectly on mobile, tablet, and desktop
- **Accessibility** — Supports reduced motion preference

## How to Customize

### Edit Letter Content

Open `index.html`, find `CONFIG.text` around line 707:

```javascript
text: {
    browserTitle: '致我最爱的你 - 情人节快乐',
    pageTitle: 'To My Dearest',
    subtitle: '情人节快乐！',
    greeting: '亲爱的宝贝：',
    signature: '永远爱你的',
    signatureName: 'Your Love',
    // ...
}
```

### Change Letter Body

Find `loveLetter` variable around line 726 and modify the letter text:

```javascript
loveLetter: `今天是情人节，我想用这封信，把平时说不出口的话都告诉你。
...
`
```

### Replace Music

Place your music file (e.g., `love.mp3`) in the same folder as `index.html`, then update:

```javascript
music: {
    src: 'love.mp3',  // Your music filename
    // ...
}
```

### Adjust Animation

Find these configurations in `CONFIG`:

| Config | Description | Default |
|--------|-------------|---------|
| `hearts.interval` | Heart spawn interval (ms) | 850 |
| `hearts.probability` | Heart spawn probability (0-1) | 0.66 |
| `fireworks.burstCount` | Fireworks per burst | 5 |
| `typing.normalDelay` | Normal char typing speed (ms) | 62 |

Higher values mean denser animations but may cause lag on mobile devices.

## File Structure

```
love-page/
├── index.html    # Main page (all code included)
├── music.mp3     # Background music (add your own)
└── README.md     # Documentation
```

## Deployment

This is a pure static HTML page — deploy to any static hosting:

- GitHub Pages
- Vercel
- Netlify
- Alibaba Cloud OSS
- Tencent Cloud COS

## Browser Compatibility

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Local Preview

Double-click `index.html` to open in browser. If music doesn't play, make sure `music.mp3` is in the same directory.

---

Made with ❤️