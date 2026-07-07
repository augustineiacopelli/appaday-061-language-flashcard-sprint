# AppADay 061 — Language Flashcard Sprint

Part of the [AppADay](https://augustineiacopelli.github.io/appaday/) project: one complete, functional, mobile-friendly web app shipped every day.

## What it does

Pick a language and a level, and get five fresh vocabulary flashcards a day, generated live by Claude. Each card is a paper index card that flips in place: the front shows the word and its part of speech, the back shows the translation and an example sentence with its own translation. Mark each card "Got It" or "Still Learning," and once all five are done for the day, a chalk streak stamp on the home screen ticks up by one. A running word history lets you flip back through everything you have already seen.

## Category

Educational (E), AI-powered.

## How it works

The app runs entirely client-side as a single HTML file. Your Claude API key, chosen language, and level are stored only in your browser's local storage, never sent anywhere but directly to the Anthropic API. Each day's card request excludes your most recently seen words so the same vocabulary does not repeat too often. Progress, streak, and word history all persist locally, so closing the tab and coming back later picks up right where you left off.

## Tech

Single-file vanilla HTML, CSS, and JavaScript. No build step, no framework. Calls the Anthropic Messages API directly from the browser using `claude-sonnet-4-6`.

## Live

https://augustineiacopelli.github.io/appaday-061-language-flashcard-sprint/
