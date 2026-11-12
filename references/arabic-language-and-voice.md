# Arabic language, voice, and on-screen text

## Default register

Use Modern Standard Arabic (العربية الفصحى المعاصرة) by default. Aim for natural, clear, spoken-friendly phrasing—not stiff literal translation and not unnecessary classical ornament. Adjust vocabulary to a general Arab audience; explain unfamiliar specialist terms briefly.

## Writing standards

- Use correct spelling, hamza, taa marbuta, ya/alif maqsura, punctuation, and agreement.
- Prefer short, well-shaped sentences for narration. Vary rhythm; avoid repeated sentence openings and excessive passive voice.
- Keep terms consistent throughout a project. Maintain a glossary for names, technical terms, and transliterations.
- Do not translate personal names or historical place names inconsistently. Record the preferred Arabic form and any accepted alternatives.
- Add diacritics selectively where ambiguity or TTS pronunciation requires them; do not vocalize every word automatically.
- Preserve exact sacred/religious quotations as verified; never “improve” their wording for rhythm.
- Separate narration, character dialogue, captions, labels, quotations, source notes, and pronunciation instructions.

## Voice and TTS preparation

- Select voice age/timbre/performance only as a creative direction; do not imply that a generated voice belongs to a real historical or religious person.
- Provide a pronunciation sheet for difficult names, foreign words, numbers, dates, and specialist terms.
- Test a short sample before generating a long voice track. Listen for hamza, emphatic consonants, taa marbuta endings, case endings where vocalized, numbers, dates, and foreign names.
- Punctuate for breathing and meaning, not merely grammar. Avoid artificial pauses inside a noun phrase or between a preposition and its noun.
- If the TTS engine mispronounces a word, try a verified pronunciation hint, selective tashkeel, alternate punctuation, or a revised but equivalent sentence. Do not distort a quotation.
- Align word/phrase timings to actual audio output, not estimated timings alone.
- Keep voice files and API credentials private. Never print keys or include them in project assets.

## RTL and typography

- Verify right-to-left layout in the actual renderer, not just in a text editor.
- Check Arabic shaping/ligatures, mixed Arabic-English text, numerals, punctuation, parentheses, and line wrapping.
- Choose a font with reliable Arabic glyph coverage and a license suitable for the intended use. Test at phone size and in the target export resolution.
- Avoid excessive text on screen. Keep captions readable, high-contrast, and safely inside platform margins.
- Subtitle timing must follow the performed voice. Do not rely on word counts or a guessed speech rate.
- Review subtitles on a real render because RTL punctuation and mixed-direction text may differ from previews.
