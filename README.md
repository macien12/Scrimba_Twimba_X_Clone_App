# Twimba — X / Twitter Clone

A small social feed app built with HTML, CSS, and vanilla JavaScript as part of the Scrimba Fullstack Developer Path. Post tweets, reply to conversations, and interact with a sample feed. Changes are saved in your browser using `localStorage`.

## Features

- Create tweets that appear at the top of the feed.
- Like and unlike tweets, with updated counts and icon colors.
- Toggle retweets, with updated counts and icon colors.
- Show or hide a tweet's replies.
- Add replies using an inline comment form.
- Delete tweets and replies you created.
- Keep tweets, replies, and interactions after refreshing the page.

## Tech stack

- HTML and CSS for layout and styling.
- Vanilla JavaScript with ES modules, event delegation, and DOM rendering.
- Vite for development and production builds.
- UUID via JSPM for identifiers on new tweets and replies.
- Font Awesome for icons and Google Fonts for the Roboto typeface.

## Available commands

| Command | Description |
| --- | --- |
| `npm start` | Start the Vite development server. |
| `npm run dev` | Start the same development server. |
| `npm run build` | Create a production build in `dist/`. |
| `npm run preview` | Serve the production build locally after building. |

## Using the app

1. Enter a message in **What's happening?** and click **Tweet**.
2. Click the heart or retweet icon to toggle an interaction.
3. Click the comment bubble to show or hide existing replies.
4. Click the reply arrow to open the reply form, type a message, and click **Comment**.
5. Click the trash icon on one of your tweets or replies to delete it.

## Project structure

```text
.
├── images/         # Profile pictures
├── data.js         # Sample tweets and replies
├── index.html      # Page markup and external stylesheets
├── index.css       # App styles
├── index.js        # Feed rendering, interactions, and local storage
├── package.json    # Dependencies and npm scripts
└── vite.config.js  # Vite configuration
```

## Data and persistence

On first use, the feed loads the sample tweets from `data.js`. After an interaction, the app saves the feed under the `tweetsData` key in `localStorage` and restores it on subsequent visits.

To reset the feed, run this in your browser's developer console and refresh the page. This removes your saved tweets, replies, and interactions for the current origin:

```js
localStorage.removeItem('tweetsData')
location.reload()
```

This is a frontend learning project with a fixed posting profile. Data stays in the current browser and origin; there is no backend, sign-in, or synchronization between users or devices. Retweeting toggles a count and icon state.

## Credits

Based on the Twimba project from the [Scrimba Fullstack Developer Path](https://scrimba.com/fullstack-path-c0fullstack), extended with replies, deletion of your own posts and replies, and browser persistence.
