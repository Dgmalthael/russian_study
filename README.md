[README.md](https://github.com/user-attachments/files/28149233/README.md)
# Russian Grammar & the Six Cases — A1 → C1

A single-page, bilingual study reference for learning Russian. Thirty chapters covering the alphabet through advanced syntax, every grammatical case explained, interactive verb conjugation cards, a 50-question verb test, a level-by-level CEFR roadmap, and a fluency appendix.

**Russian title:** *Русская грамматика и падежи*

## What's inside

A static HTML file (no build step, no dependencies) that opens as a complete grammar handbook.

### Five parts + appendices

1. **Foundations** — alphabet, gender, number, what cases do, the spelling rules
2. **The Six Cases** — nominative, accusative, genitive, dative, instrumental, prepositional, plus a preposition → case map
3. **Declension** — noun, adjective, pronoun, numeral declension tables
4. **The Verb System** — basics, present, past, future, aspect, motion verbs, imperative, conditional, reflexives, verb government
5. **Advanced Grammar** — participles, verbal adverbs, word order, subordinate clauses (deep dive on `который`), word formation, impersonal constructions and negation

### Appendices

- **A.** Master ending chart
- **B.** CEFR level map
- **C.** Grammar glossary (Russian ⇄ English)
- **D.** Master grammar grid — every case on one page
- **E.** Core vocabulary with live search
- **F.** Essential verbs (~250) with click-to-expand conjugations
- **G.** 50-question randomised verb test
- **H.** CEFR Roadmap A1 → C1 — what you should be able to do at each level
- **I.** Fluency & idiom — fillers, collocations, polite expressions, idioms

## Features

- **Bilingual** — every grammar term, example, and table is presented in Russian with English translation
- **Stress marks** on key vocabulary (`хорошо́`, `молоко́`)
- **Inline pronunciation transcriptions** under examples (`KHA-ra-SHÓ`)
- **Click-to-expand verb cards** — 15 illustrated cards in Chapter 17 (быть, хоте́ть, есть, дать, идти́/ходи́ть, е́хать/е́здить, люби́ть, ви́деть, мочь, жить, писа́ть, говори́ть/сказа́ть, чита́ть, знать, понима́ть) showing present, past, future, imperative, government and collocations
- **Inline verb conjugator** — click any of the ~250 verbs in Appendix F to expand a panel with full forms, all on the page. 109 verbs are hand-curated for accuracy; the rest are algorithmically conjugated and tagged `auto`
- **Live search filters** — table of contents, vocabulary list, and verb list each have a real-time filter
- **50-question verb test** — randomised every time you press the button, with score and missed-question review
- **Self-check quizzes** embedded throughout chapters — click an option, see whether it's right and why
- **CEFR-mapped study path** — five level summary cards (A1 → C1) with I-can statements, grammar checkpoints, vocabulary targets, study-hour estimates, and chapter cross-references
- **Verb government reference** — verbs grouped by which case they force on their complement
- **Special deep-dive sections** on `который` (with full declension table and 6 worked examples), aspect, motion verbs, and the genitive of negation
- **Responsive layout** with a collapsible sidebar on mobile
- **Print-friendly** — sidebar, quizzes and toggles hide for clean printout

## Getting started

```
git clone <your-repo-url>
cd learnrussian
```

Open `index.html.html` in any modern browser. There is no build step and no server required.

Or simply double-click the file in a file manager.

## File structure

```
learnrussian/
├── README.md
├── index.html.html         — the entire reference (single file, ~6 200 lines)
└── assets/
    └── automatedev-logo.png
```

Everything — markup, CSS, and JavaScript — lives in one HTML file. The only external resource is the Google Fonts stylesheet for Playfair Display, PT Serif, PT Sans, and JetBrains Mono.

## Tech stack

- Vanilla HTML5, CSS, and JavaScript — no framework, no bundler
- Google Fonts: Playfair Display (display serif), PT Serif (body), PT Sans (UI), JetBrains Mono (transcriptions)
- CSS custom properties for the brand palette (deep blue → purple → magenta)
- All interactivity is plain `document.querySelectorAll` + class toggles; no virtual DOM, no state library

## Customization

Open `index.html.html` and look at the `:root` block near the top of the `<style>` element. The brand palette is defined as CSS variables:

```css
--brand-blue:#3a3fc9;
--brand-purple:#8b2fe0;
--brand-pink:#e91fb1;
--c-nom:#2a37b5;   /* nominative accent */
--c-acc:#e91fb1;   /* accusative accent */
--c-gen:#8b2fe0;   /* genitive accent */
...
```

Change those values and the entire page restyles.

To add more verbs to the inline conjugator's curated dictionary, find the `var IRR = { ... }` object in the last `<script>` block and add an entry of the shape:

```js
'инфинити́в':{
  impf:true,                                              // or false for perfective
  pres:['я-form','ты-form','он-form','мы-form','вы-form','они-form'],
  past:['masc','fem','neut','plural'],
  imp:['ты-form','вы-form'],
  note:'Optional note about irregularity'
}
```

For perfective verbs, use `fut` instead of `pres`. For `быть`-style verbs with no present, use `futCmp` for the compound future of `быть`.

## Learning path

A suggested order for working through the reference, mapped to the CEFR levels:

| Level | Focus | Chapters |
|-------|-------|----------|
| A1 | Alphabet, gender, present tense, nom/acc/prep | 1–7, 11, 17 |
| A2 | All six cases (sg), past & future, intro to aspect | 5, 8–10, 18, 21, 23 |
| B1 | Full plural declension, aspect, motion verbs, conditional, `который` | 13–16, 19, 20, 22, 24, 28 |
| B2 | Participles, verbal adverbs, complex sentences, impersonal | 25–27, 30 |
| C1 | Word formation, register, idiom, aspect nuance | 27, 29, 30 + review |

The full roadmap with hour estimates and vocabulary targets is in **Appendix H** on the page.

## Browser support

Tested on current Chrome, Firefox, Edge and Safari. Requires support for CSS Grid, CSS custom properties, and ES5 JavaScript (no transpilation needed).

## Credits

Created by **AutomateDev**. Connect on [LinkedIn](https://www.linkedin.com/in/u-deniz-geles/).

The CEFR descriptors and level-progression structure follow the [Common European Framework of Reference for Languages](https://en.wikipedia.org/wiki/Common_European_Framework_of_Reference_for_Languages). The inline conjugator's "verify ↗" links point to [Cooljugator](https://cooljugator.com/ru/) as an external double-check for irregular forms.



---

Уда́чи в изуче́нии ру́сского языка́! — Good luck with your Russian.
