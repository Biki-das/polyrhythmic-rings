# Polyrhythmic Rings

![My GIF](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMnYxejc2NGZ4YnFvbDY5ZGx5d2NzeGV1ZDFndDNqcjE4ZGsxemVqbCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xp5W1xFyKynS2uJWVz/giphy.gif)

Relaxing tunes and visuals to help you focus, meditate, or sleep. Project inspired by [Hyperplexed's video](https://www.youtube.com/watch?v=Kt3DavtVGVE) on their YouTube channel.


## Built Using

- [Next.js](https://nextjs.org/)
- [SVGs](https://developer.mozilla.org/en-US/docs/Web/SVG)
- [Framer Motion](https://www.framer.com/motion/)
- [Radix UI](https://www.radix-ui.com/)

## Installation

> Note: You need to have Node.js and npm installed on your machine before following these steps.

```
git clone https://github.com/Biki-das/polyrhythmic-rings.git
cd polyrhythmic-rings
npm install
npm run dev
```

Now, open your browser and navigate to `http://localhost:3000` to see the application running.

## Cross-Browser Caveats & Performance Issues

One of the most performance intensive parts of the application is the horizontal strings that trigger when the white circles hit them. I faced severe performance issues in Safari and Firefox. I tried two methods to solve this.

First by using SVG filters on an SVG `<line />` element, and the second, using the same filters on an HTML `<div />`. The first method performs well for Safari, but is very sluggish for Firefox, however the second method is very sluggish for Safari, and just marginally better for Firefox. We're currently using the SVG `<line />` in production, but both versions are available in the project files.

I'll continue to work on this, I have a few new ideas to try out.
