---
title: "URL as a Skill"
date: 2026-03-16
description: "Using the URL bar intentionally can make navigating the web faster and smarter. These are a few insights I picked up about URLs while building and using web apps."
tags:
  - "Web"
  - "Productivity"
  - "Browsers"
---

## I rarely see the GitHub homepage.

If I want a repo, I type the repo URL. If I want a profile, I type the profile URL. If I want issues or pull requests, I just change the last part of the URL.

No clicking through the UI. No menus. Just the URL bar.

At some point I noticed something interesting. The more time you spend online, the more the URL bar starts feeling less like a place where you type websites and more like a navigation tool.

## When you start noticing patterns

When you first use a website, you rely completely on the interface.

- Click the button.
- Open the menu.
- Follow links.

But after using the same site for a while, patterns start appearing. GitHub is a simple example.

```text
github.com/{username}
github.com/{username}/{repo}
github.com/{user}/{repo}/issues
github.com/{user}/{repo}/pulls
```

If you are on `/issues` and want pull requests, you can just change it to `/pulls`. No navigation needed.

## More Examples

### Going directly to problems on LeetCode

On coding platforms like LeetCode, I rarely open the homepage anymore.

```text
leetcode.com/problems/{problem-name}
leetcode.com/problems/{problem-name}/submissions/
leetcode.com/u/{username}
```

Once you know the structure, you can jump directly to where you want to go.

### Switching between Google accounts

Google services follow a similar pattern. For example in Gmail, the number after `/u/` represents the account index.

```text
https://mail.google.com/mail/u/0/#inbox
https://mail.google.com/mail/u/1/#inbox
https://mail.google.com/mail/u/2/#inbox
```

Changing that number switches the account instantly. Works across many Google products.

### Jumping to a specific video moment

YouTube links support timestamps using the `t` query parameter.

```text
youtube.com/watch?v=VIDEO_ID&t=300
```

This opens the video at 300 seconds. People often share links like this when pointing to a specific part of a video.

### Finding any npm package

npm works the same way. Once you know the URL pattern, you never really need to search the homepage.

```text
npmjs.com/package/{package-name}
npmjs.com/package/react
npmjs.com/package/tailwindcss
```

### Vercel preview deploys

Vercel preview deployments are another good example.

Every pull request gets its own predictable preview URL. You can open it directly, share it, or test it without navigating the dashboard.

Production, staging, preview builds. Each environment has its own URL. The URL itself is already telling you where you are.

### Slugs: readable URLs for content pages

You are reading this blog at `/blog/url-as-a-skill`. That last part is called a **slug**.

A slug is basically a URL-friendly version of a title.

```text
"URL as a Skill"  →  url-as-a-skill
"My First Post"   →  my-first-post
"What is Next.js" →  what-is-next-js
```

The rules are pretty simple:

- Lowercase everything.
- Replace spaces with hyphens.
- Remove special characters.

Slugs make URLs readable and shareable. They also help with SEO because search engines understand the words in the path.

```text
/blog?id=f3a92c          ← tells you nothing
/blog/url-as-a-skill    ← tells you exactly what it is
```

Most modern frameworks like Next.js use file-based routing, where the folder name literally becomes the slug.

## Why this actually matters

1. It is faster than navigating through menus.
2. You start noticing route patterns like `/users` `/repos` `/issues` `/settings`.
3. It also helps when building webapps because routing in React, Next.js, or Express follows the same idea.

## How to develop this habit

- Pay attention to the address bar when moving between pages.
- Notice path changes like `/issues` to `/pulls`.
- Try editing URLs manually and see what happens.
- Watch for common paths like `/profile` `/dashboard` `/settings` `/docs` `/api` `/admin`.

<p class="post-outro">The URL bar is the command line of the web.</p>
