# GenAI tips from the Eden Centre

A collection of the weekly GenAI tips posted in the Eden Centre's AI and Education channel in Microsoft Teams at LSE. Each tip is a short, practical idea for using GenAI tools such as Claude and Microsoft Copilot in everyday work, with a prompt to try.

**View the tips:** https://hedgehoginthefogg.github.io/eden-ai/

The tips and pictures are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), so you're welcome to share and adapt them with credit.

## Using the page

- **Arrange the cards:** view them by date (oldest first), gathered into category piles, scattered across the table or shuffled. Select a category pile to spread its cards out.
- **Search:** type a word or phrase to filter the cards. Every word you type must appear in the tip's headline, text, prompt or category.
- **Read a tip:** select a card to open it full size, with the tip, its "Try this" prompt and why it works. Use "Previous tip" and "Next tip" to move through the cards in their current order.
- **Copy a prompt:** select "Copy prompt" and paste it into a new chat.
- **List view:** shows every tip as text, which suits screen readers and quick scanning.
- **Link to a tip:** each tip has its own address. For example, `#tip-4` at the end of the page address opens tip 4.

## What's in this repository

| File | What it is |
|---|---|
| `index.html` | The whole page: tips, pictures, fonts and code in one self-contained file. It makes no requests to other sites, so it also works saved to your computer and opened offline. |
| `README.md` | This file. |
| `LICENSE` | The licence for the tips, pictures and page (CC BY 4.0). |

## Updating the page

The page is exported from the GenAI tip image maker, a Claude Artifact used by the Eden Centre to write the tips and make their images.

1. In the image maker, tick **Posted in the channel** on each tip once it has gone out in Teams, and check the date beside it.
2. Select **Export tips page (HTML)** and save the file. It's called `index.html`.
3. In this repository on GitHub, select **Add file**, then **Upload files**, and upload the new `index.html` to replace the old one.
4. Add a short commit message, such as "Add tips posted in November", and select **Commit changes**.

GitHub Pages republishes the site automatically, usually within a few minutes.

Tips are numbered in the order they were posted, so the numbers on the page match the images in Teams as long as tips are posted in the order they're listed in the image maker.

## Setting up GitHub Pages (first time only)

1. In this repository, select **Settings**, then **Pages** in the "Code and automation" section of the sidebar.
2. Under "Build and deployment", set **Source** to **Deploy from a branch**.
3. Choose the `main` branch and the `/ (root)` folder, then select **Save**.

After a few minutes, the page's address appears at the top of the Pages settings. On a free GitHub plan, Pages only works for public repositories, and the published site is public either way. Only commit content that's fine for anyone to read.

Optionally, add an empty file called `.nojekyll` to the repository. This tells GitHub to publish the files as they are, without running its Jekyll site builder, which makes updates a little quicker.

## Privacy and accessibility

- **Privacy:** the page doesn't use cookies, analytics or tracking. Searching and copying happen entirely in the visitor's browser.
- **Keyboard:** every card, pile and button can be reached and used with a keyboard.
- **Screen readers:** each card has a text label, and every picture has alt text.
- **Motion:** the dealing, shuffling and scattering animations switch off for anyone who has set their device to reduce motion.
- **Display:** the page adapts to light and dark mode and to screen sizes from phones to large monitors.

If anything on the page doesn't work with the assistive technology you use, please get in touch (see Contact).

## Credits and licences

- **Licence:** the tips, their pictures and the page are licensed under the [Creative Commons Attribution 4.0 International licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You can share and adapt them for any purpose, including commercially, as long as you give credit, link to the licence and say if you made changes. Please credit them as "GenAI tips from the Eden Centre, LSE, licensed under CC BY 4.0". See `LICENSE` for details.
- **Tips and pictures:** written and drawn for the Eden Centre, LSE, with help from Claude.
- **Fonts:** [Atkinson Hyperlegible](https://www.brailleinstitute.org/freefont/) (Braille Institute), [Newsreader](https://github.com/productiontype/Newsreader) (Production Type) and [Courier Prime](https://github.com/quoteunquoteapps/CourierPrime) (Quote-Unquote Apps). All three are licensed under the [SIL Open Font License 1.1](https://openfontlicense.org) and are embedded in `index.html`. The fonts aren't covered by the CC BY licence.

## Contact

Steven Williams, AI and Education Specialist, Eden Centre and Digital Skills Lab, LSE: s.williams10@lse.ac.uk
