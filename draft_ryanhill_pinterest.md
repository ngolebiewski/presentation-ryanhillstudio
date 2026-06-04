---
marp: true
theme: default
class: lead
paginate: true
backgroundColor: #191d23
color: #CCD5E5
style: |
  /* Inspration: Techbase Color Scheme */
  /* Source at: https://github.com/mcauley-penney/techbase.nvim/blob/main/lua/techbase/palettes/techbase.lua */
  
  :root {
    --normal-fg: #CCD5E5;
    --float-fg: #D6DDEA;
    --normal-bg: #191d23;
    --float-bg: #1C2127;
    --keyword: #A9B9EF;
    --string: #74BAA8;
    --search: #E9B872;
    --number: #B85B53;
    --error: #F71735;
    --important: #6A8BE3;
  }

  section h1 {
    color: var(--normal-fg) !important;
    font-weight: 700;
    font-size: 2em !important;;
  }

  section h2 {
    color: var(--string) !important;
    font-weight: 700;
    font-size: 1.4em;
  }

  section h3 {
    color: var(--error) !important;
    font-weight: 600;
    font-size: 1.2em;
  }

  section h4, section h5, section h6 {
    color: var(--keyword) !important;
    font-weight: 700;
  }

  footer {
    font-size: 1em;
    color: var(--float-fg);
    text-shadow: none !important;
    filter: none !important;
  }

  a {
    color: var(--error);
    text-decoration: underline;
  }

  code {
    background-color: var(--float-bg);
    color: var(--search);
    padding: 0.2em 0.4em;
    border-radius: 4px;
    font-family: 'Monaco', 'Courier New', monospace;
    font-size: 0.65em; /* Shrinks the font slightly so long lines fit the slide */
  }

  pre {
    background-color: var(--float-bg);
    color: var(--normal-fg);
    padding: 1em;
    border-radius: 8px;
    border-left: 4px solid var(--keyword);
    
    /* Sizing Fixes */
    width: 90%;          /* Forces the code box to span almost the full width of the slide */
    max-height: 70vh;    /* Prevents long code from spilling off the bottom of the slide */
    overflow: auto;      /* Adds scrollbars if the code block is too tall or wide */
    box-sizing: border-box; 
    align-self: center;  /* Centers the block within the parent flex section */
  }

  section {
    font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, 'Helvetica Neue', sans-serif;
    background-color: var(--normal-bg);
    color: var(--normal-fg);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  section.left {
    align-items: flex-start;
    padding-left: 2em;
  }

  section.lead h1 {
    font-size: 1.8em;
    margin: 0.5em 0;
  }

  em {
    color: #FFC0C5;
  }

  strong {
    color: var(--search);
  }

  ul {
    font-size: 0.95em;
  }

  li {
    margin: 0.3em 0;
  }

  /* Define the split utility class */
    .split-25-75 {
    display: grid;
    grid-template-columns: 1fr 3fr;
    gap: 40px;
    align-items: center;
  }
  
  /* The New 50/50 Left/Right Split */
  .split-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
  }
  
  /* Shared layout helper utilities */
  .split-25-75 .col-left, .split-50-50 .col-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .split-25-75 .col-right, .split-50-50 .col-right {
    display: flex;
    justify-content: center;
    align-items: center;
  }
---

# How to write slides

Split pages by horizontal ruler (`---`). It's very simple! :satisfied:

```markdown
# Slide 1

foobar

---

# Slide 2

foobar
```
---

# Style Showcase

## Heading 2 in Pink

### Heading 3 in Gold

- Main bullet point with _pink emphasis_
- Another point with **bold gold highlight**
- Link example: [Visit ryanhill.studio](https://ryanhill.studio)

![w:400](images/screenshot_misc_drawings.png)

---


# Nick Golebiewski

Pinterest Presentation 📌
6/12/2026

---
# Ryan Hill Studio


Nuxt artist portfolio. 
An alternative-to-Squarespace. No subscription. No data lock-in. Nearly free. All Open-Source!
A full-stack single-admin web app that puts the art first. 
[ryanhill.studio](https://ryanhill.studio)
---

# Overview
1. Demo
2. Technologies used/Design Desicions
3. Challenges
4. AI Use
5. What I Learned
6. Post Script

---
<!-- Full screen intro of project -->
![bg cover](images/screenshot_misc_drawings.png)

---

# Admin

1. Minimal interface, nothing extra
2. Drag and Drop ordering for art series and artworks in series
3. Markdown editor (Not clunky HTML WYSIWG) for content, like CV
4. 

---
<!-- Full screen image of admin dashboard -->
![bg cover](images/artwork-upload)

---
# Responsive Design


---
<!-- Slide 2: The new Desktop balanced Left/Right split (50/50) -->
<div class="split-25-75">
<div class="col-left">

### Desktop/Laptop

</div>
<div class="col-right">

<!-- Adjusted width slightly to scale cleanly within a 50% column -->
![w:800](images/ryanhillstudio-desktop-demo.gif)

</div>
</div>

---
<!-- 
We wrap the slide content in a div with our grid class.
Marp automatically handles simple HTML tags mixed with Markdown.
-->

<div class="split-25-75">
<div class="col-left">

## Mobile

</div>
<div class="col-right">

![w:300](images/ryanhillstudio-mobile-demo.gif)

</div>
</div>

---


# Technology

---
- *Frontend*: 
  - **Nuxt (Vue)**
    - SSR (Server Side Rendering)
    - Semantic Routing (Dynamic for artworks, hard coded for known pages like CV, About, Contact)
    - Wanted to try alternative to React Framework, also working on on a project written with Nuxt as front end so want to get an understanding
  - **Tailwind**
    - Responsive CSS, inline, solid
  - **TypeScript**
    - Industry Standard

---
- *Backend*: 
  - **Node**
    - Almost a built-in with Nuxt, keep project self-contained
  - **PostgreSQL**
    - Open-souce relational database
  - **Argon2**
    - Memory hardened hash cryptography, OAuth2 too heavy for scope.

---
- *DevOps*: 
  - **Netlify**
    - Netlify Blobs for image uploads
    - Netlify Serverless Functions
    - CI/CD from Github
    - Image CDN and cache speed via DNS set to Netlify nameserver from registrar
    - Deploy Previews on Pull Requests
  - **Neon**
    - Dev friendly database host, connects to Netlify
  - **Github**
    - Git repo for project
    - Netlify connection and deploy tests
    - AI: Copilot with Claude Haiku 4.5 agents
    - Issues to track project milestones

---

<div class="split-25-75">
<div class="col-left">

# Database Schema

</div>
<div class="col-right">

![w:500](images/mermaid-diagram-2026-06-03-133957.png)

</div>
</div>


---
# Challenges
---
1. Auth 
   1. User logs in and gets logged out right away
   2. Nuxt hydration issue SSR vs. client side
2. UNTITLED
   1. Have you been to an art museum and every other artowrk is titled, "Untitled"?
   2. This is a database constraint set for the URL slug based on the title of an artwork
   3. Uploads failed, so wrote a method to append a 3 digit counter in event of a duplicate.
   4. NOT THE PROBLEM THOUGH!
   5. User just needed to clear old JSON webtoken cookie from a previous session, something I already built a button to do from the admin dashboard.
   6. Found a real bug while searching for a solution to another.
3. Netlify Blobs
   1. Development - API route caching
4. Nuxt
   1. API Route naming conventions
   2. Chose to use escaped SQL rather than ORM (Go style)
...
5. Video Stream
   1. Solved partly through YouTube. Arist already on, they're ok at streaming.
   2. Get URL to stream, and video still from parsing youtube link, along with a bool check on the form.
   3. But, there's youtube "shorts", so had to add that in. 
   4. RegEx fix!

```typescript
async (newUrl) => {
    if (!newUrl || !newArtwork.value.is_video) return;

    // Handles:
    // - youtube.com/watch?v=
    // - youtu.be/
    // - youtube.com/shorts/
    // - youtube.com/embed/
    // - extra params like ?si=
    const match = newUrl.match(
      /(?:youtube\.com\/(?:watch\?v=|shorts\/|embed\/)|youtu\.be\/)([\w-]{11})/,
    );

    const videoId = match ? match[1] : null;

    if (videoId) {
      // Auto thumbnail
      newArtwork.value.image_url =
        `https://img.youtube.com/vi/${videoId}/hqdefault.jpg`;

      // Auto title via YouTube oEmbed

      try {
        const oEmbed = await $fetch(
          `https://www.youtube.com/oembed?url=${encodeURIComponent(newUrl)}&format=json`,
        );

        if (oEmbed?.title && !newArtwork.value.title) {
          newArtwork.value.title = oEmbed.title;
        }
      }...

```

--- 

# AI

Used Github AI Copilot with agents using Claude Haiku 4.5. At that time could generate a Codepsace right from the Github Issue and worked on a branch. Was really efficient with tokens. Like remarkably so compared to VS Code on my desktop. Spent time writing detailed issues. All free level. 

Could use more,

---

![bg contain](images/threads-happy-client.jpg)

---

# Thank you



Nick Golebiewski
Site: [ryanhill.studio](https://ryanhill.studio/)
Code: [github.com/ngolebiewski/ryan-hill-studio-v2/](https://github.com/ngolebiewski/ryan-hill-studio-v2/)