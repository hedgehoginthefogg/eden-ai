# Working with GenAI in 2026/27: GenAI tips from the Eden Centre

A collection of the short GenAI posts shared every weekday in the Eden Centre's AI and Education channel in Microsoft Teams at LSE. Each week has three practical tips, an AI at LSE update and a news story, grouped into themed collections. The aim is to help colleagues change how they think about, talk about and use GenAI in their work, and to pick out what actually matters from the constant stream of AI news.

**View the tips:** https://hedgehoginthefogg.github.io/eden-ai/ (short link: https://tinyurl.com/edenaitips)

The series is a trial, run by Jamie Hayward and Steven Williams (AI and Education Specialists), before something similar is created for the wider School on the AI and Education Toolkit. Feedback and suggestions for topics are welcome (see Contact).

The tips and pictures are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), so you're welcome to share and adapt them with credit.

## Using the page

Until the first tip is posted, the page shows a short note saying cards will appear as they're posted. Some features appear once there are enough tips for them to be useful: the quiz and "Shake for a tip" at 5 tips, the ways of arranging the cards and "Match the pairs" at 6, "Find the rogue bot" at 8 and search at 10.

- **Watch the trailer:** a 36-second introduction to the series, with a text description of every scene and an accessible PDF version. After the first week, it shrinks to a one-line "Watch the 36-second trailer" link.
- **Arrange the cards:** view them by date (oldest first), gathered into category piles, scattered across the table or shuffled. Select a category pile to spread its cards out.
- **Search:** type a word or phrase to filter the cards. Every word you type must appear in the tip's headline, text, prompt or category.
- **Read a tip:** select a card to open it full size, with the tip, its "Try this" and why it works (or why it matters), plus a further reading link where there is one. If a tip has a video, it appears at the top in place of the card picture. Use "Previous tip" and "Next tip" to move through the cards in their current order.
- **Copy a prompt:** select "Copy prompt" and paste it into a new chat.
- **Quiz yourself:** answer a question about each card from memory, rate how sure you are, then compare your answer with the model answer. Choose a random mix, one category or cards you pick, and play alone, with someone on the same device, or with someone on another device using a short code or link.
- **Match the pairs:** a memory game. Turn over two cards at a time to match each tip with its key idea, in as few goes as you can.
- **Find the rogue bot:** a bot hides under one of the cards. Read the clue, which names a card's key idea, and pick the right card before the bot hides again.
- **Shake for a tip:** on a phone, shake your phone to rattle a catalogue drawer, and a random card pops out. There's also a "Pick a card" button for anyone who can't or doesn't want to shake.
- **Add to your home screen:** on a phone or tablet, select "Add these tips to your home screen" to keep the tips like an app. They work offline once opened, apart from videos.
- **List view:** shows every tip as text, which suits screen readers and quick scanning.
- **Link to a tip:** each tip has its own address, made from its headline. For example, `#your-chatbot-has-a-computer` at the end of the page address opens that tip.

## What's in this repository

| File or folder | What it is |
|---|---|
| `index.html` | The whole page: tips, pictures, fonts and code in one file. Apart from the files in `videos/` and the trailer PDF, it makes no requests to other sites. |
| `manifest.webmanifest` | Describes the page as an app (name, colours and icons) so it can be added to a phone's home screen. |
| `sw.js` | A service worker that keeps the page working offline. It always tries the internet first, so new tips appear as soon as they're published. It doesn't store videos or PDFs. |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | The app icons for Android and iPhone home screens. |
| `genai-tips-trailer-description.pdf` | An accessible PDF describing the trailer, for anyone who can't watch it. |
| `videos/` | The trailer and its poster image, and each tip's videos, thumbnails, captions and text versions. |
| `README.md` | This file. |
| `LICENSE` | The licence for the tips, pictures and page (CC BY 4.0). |

## Privacy and accessibility

- **Privacy:** the page doesn't use cookies, analytics or tracking. Searching, quizzes, games and copying happen entirely in the visitor's browser, and best scores are stored only on their device.
- **Keyboard:** every card, pile, game and button can be reached and used with a keyboard.
- **Screen readers:** each card has a text label, every picture has alt text, and links that open in a new tab say so.
- **Video:** tip videos have captions where they include speech, and each has a text version. The trailer has no sound and comes with a text description and an accessible PDF.
- **Motion:** the dealing, shuffling, scattering and flipping animations switch off for anyone who has set their device to reduce motion.
- **Display:** the page adapts to light and dark mode and to screen sizes from phones to large monitors.

If anything on the page doesn't work with the assistive technology you use, please get in touch (see Contact).

## How these tips were made

Steven Williams designed the series and built it using Claude (Anthropic). Claude drafted tips, quiz questions and game clues from his notes, workshop materials and articles, drew the card pictures as code, and wrote the code for the image maker, this page and its games, and the trailer video. Every tip is edited and checked against its sources before it's posted. The page itself has a fuller "How these tips were made" section at the bottom.

## Credits and licences

- **Licence:** the tips, their pictures, videos and the page are licensed under the [Creative Commons Attribution 4.0 International licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You can share and adapt them for any purpose, including commercially, as long as you give credit, link to the licence and say if you made changes. Please credit them as "GenAI tips from the Eden Centre, LSE, licensed under CC BY 4.0". See `LICENSE` for details.
- **Fonts:** [Atkinson Hyperlegible](https://www.brailleinstitute.org/freefont/) (Braille Institute), [Newsreader](https://github.com/productiontype/Newsreader) (Production Type) and [Courier Prime](https://github.com/quoteunquoteapps/CourierPrime) (Quote-Unquote Apps). All three are licensed under the [SIL Open Font License 1.1](https://openfontlicense.org) and are embedded in `index.html`. The fonts aren't covered by the CC BY licence.

## Contact

Jamie Hayward and Steven Williams, AI and Education Specialists, Eden Centre and Digital Skills Lab, LSE. Questions, corrections, feedback and suggestions: s.williams10@lse.ac.uk
