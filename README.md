# Scroll Animation with CSS View Timeline

![Scroll Animation Demo](https://img.shields.io/badge/Demo-Scroll%20Animations-orange)
![CSS](https://img.shields.io/badge/CSS-View%20Timeline-blue)
[![YouTube](https://img.shields.io/badge/YouTube-chunkydotdev-red)](https://youtube.com/@chunkydotdev)

A showcase of modern scroll-based animations using the CSS `view-timeline` property, without any JavaScript!

## 🌟 Project Overview

This project demonstrates how to create engaging scroll animations using pure CSS with the modern `view-timeline` property. Each section showcases a different animation technique that triggers as you scroll:

1. **Hero Section** - Fade effects
2. **Split Section** - Panels sliding from both sides
3. **Card Stack** - Cards spreading out in a fan effect
4. **Text Motion** - Text flowing across the screen from alternate sides
5. **Final Section** - Gradient transition with fade effects

## 📚 What is View Timeline?

The CSS View Timeline feature allows you to create scroll-linked animations without JavaScript. It's part of the [CSS Scroll-driven Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll-driven_animations) specification.

### Key Components:

- **`view-timeline-name`**: Names a timeline based on an element's position in the viewport
- **`view-timeline-axis`**: Defines the axis (block/inline) for measuring the element's progress
- **`animation-timeline`**: Binds an animation to a view timeline
- **`animation-range`**: Defines when the animation starts and ends in relation to the view timeline

## 🎯 How It Works

Each section creates its own timeline:

```css
.section {
  view-timeline-name: --section-timeline;
  view-timeline-axis: block;
}
```

Elements are animated as the section moves through the viewport:

```css
.animate-title {
  animation: fade-up 1s linear forwards;
  animation-timeline: --section-timeline;
  animation-range: cover 50% cover 90%;
}
```

## 🚀 Animation Examples

### Sliding Panels

```css
.split-half.left {
  animation: slide-right 1s linear forwards;
  animation-timeline: --section-timeline;
  animation-range: entry 20% cover 40%;
}
```

### Card Fan Effect

```css
.card {
  animation: fan-out 1s linear forwards;
  animation-timeline: --section-timeline;
  animation-range: entry 20% cover 60%;
}
```

### Moving Text

```css
.text-line:nth-child(odd) {
  animation-name: move-left-to-right;
  animation-timeline: --section-timeline;
  animation-range: entry 0% exit 100%;
}
```

## 📱 Browser Support

The `view-timeline` property is relatively new and is supported in:
- Chrome 115+
- Edge 115+
- Safari 16.4+
- Firefox 116+

For older browsers, you would need to use JavaScript alternatives like Intersection Observer.

## 📖 Learning Resources

To dive deeper into CSS view timelines:

- [CSS Scroll-driven Animations on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_scroll-driven_animations)
- [View Timeline examples on web.dev](https://developer.chrome.com/blog/scroll-animation/)
- [Using CSS Animations on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animations/Using_CSS_animations)

## 🔍 Project Structure

- **index.html** - The structure with sections for each animation type
- **styles.css** - All the animation logic using view-timeline
- No JavaScript required!

## 🎬 See It in Action

Check out the full tutorial and demo on my YouTube channel: [chunkydotdev](https://youtube.com/chunkydotdev)

## 🤝 Contributing

Feel free to fork this repository and experiment with your own scroll animations!

## 📃 License

MIT License - Feel free to use and modify for your own projects.

---

Made with ❤️ by [chunkydotdev](https://youtube.com/chunkydotdev)
