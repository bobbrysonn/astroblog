---
title: How to Use Icons in Gyoza?
date: 2024-05-08T10:54:27.000Z
tags: [Icon]
category: Tutorial
comments: true
draft: false
---

Gyoza uses the **font-class** method for referencing icons.  
Most of these icons come from [Remix Icons](https://remixicon.com/) and are managed/exported through [iconfont](https://www.iconfont.cn/).

Here’s an overview of all the icons included in the project:

![All icons](https://s2.loli.net/2024/05/08/mbdT5HqYMEajyRG.webp)

When adding social accounts for display on the homepage, you may want to use these icons.  
Just fill in the name shown under the icon (with the `icon-` prefix) in the corresponding config field.

If you’re using icons inside a component, you can do it like this:

```jsx
<i className="iconfont icon-xxx"></i>
```

## Why Not SVG Icons?

You might have seen many projects using [iconify](https://iconify.design/).
Iconify is an open-source icon set with over 200,000 icons and provides integration for multiple frameworks. Astro also has a plugin called [astro-icon](https://github.com/natemoo-re/astro-icon) that makes it easy to use.

I actually tried iconify in this project, but for several reasons I ended up sticking with the font-class approach:

- The project mixes Astro and React components. Iconify icons are used differently in each, which would force me to maintain two separate usage patterns in the codebase.
- Iconify loads icons by requesting from their server. ~~I worried about request failures~~ (though admittedly this is unlikely).
- I inject icons into markdown at render time (e.g. an external link indicator). Doing this with iconify is less convenient.
- Directly embedding lots of SVG icons in HTML feels messy. With font-class, you only need a class name. The final HTML is slightly smaller, which should make page loads a bit faster (not benchmarked, but still a consideration).
- The project doesn’t use many icons — mostly common social account logos for custom contact links. Having all icons managed in one place feels simpler.

That said, I have to admit this solution isn’t perfect. Every time the icon set changes, I need to update both the font files and the CSS. It also makes it harder for others to manage the collection.

Maybe in the future I’ll experiment with alternatives like [@iconify/tailwind](https://github.com/iconify/iconify/tree/main/plugins/tailwind).
If you’ve got a better idea, feel free to leave me a comment!

## Custom Icons

If you’d like to replace the default iconfont set, update the following files:

```text
public/fonts/iconfont.ttf
public/fonts/iconfont.woff
public/fonts/iconfont.woff2
src/styles/iconfont.css
```

⚠️ Note: This will replace **all** icons used in the project, so make sure you know what you’re doing before making changes.

```

---

This way the guide flows naturally for an English-speaking audience but still keeps your reasoning and dev details.

👉 Do you want me to also make the tone a bit **more casual (like “my thoughts on icons”)** or keep it **practical/documentation-style**?
```
