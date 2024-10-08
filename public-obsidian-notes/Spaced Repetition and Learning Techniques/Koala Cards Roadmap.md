### Problems
- "wrong" grading and rollback refactor
- We don't cache correct responses, leading to increased cost.
- Changing ones mind mid recording is not possible.
- Use GCS instead of B64 strings for Audio (Firefox memory leak)
- Need a "Refresh" button for incorrect card illustrations, such as the card "Await the order".
- Need a "Refresh" button for bad translations.
- Hitting "AGAIN" on the first card of a session causes weird behavior.
- Review UI and Learn UI are shared currently.
	- The "AGAIN" button is not  really correct in this context. Should just be a 0-4 scale of difficulty.
#### Small Features
- Integrate PostHog to see usage patterns and get feedback
- Force 100% recitation of failed cards in same session.
- Store audio in Google Cloud, not B64.
- Always play audio back even if difficulty is not AGAIN
- Add a "refresh" button to the final page of the "Add Cards" flow for when it doesn't come out quite right.
- Include the card front/back when sending transcription to Whisper (might reduce transcription error rate).
- Add a "disagreement count" column to identify problematic / confusing cards.
- An "Ask Again" button when a response is disputed.
### Routine Features
 * Once there are no more cards for review, transition to "cram mode" which reviews cards in difficulty order and does typing / speaking tests with no grading.
 * Decks
 * Shared Decks
 * "Review Radio"
	 * Experiment in progress.
 * Ability to attach notes to cards
 * New Card types
	 * Listening only
	 * Image identification (for nouns)
	 * Listening / reading comprehension (theme + vocabulary word = machine generated paragraph and followup questions)
	 * Typing (a dictation test for spelling)
 * Learning session options (listening only, one deck only, one language only, etc)
 * Card progression (dictation => Reading => Listening => Speaking)
 * FSRS Revlog
 * Card notes that are shown/added on failure.
### Crazy Ideas

 * [[Situation and Goal Language Drills]]
 * After every correct answer, run it through a grammar correction and improvement pass. Vectorize all feedback, perform clustering, create a list of improvement goals.
 * Ability for students to link teachers or tutors to their account.
	 * Share top N most difficult cards
	 * Voice recording submission to teacher for pronunciation feedback
### Koala Cards
 * [[Koala Cards Roadmap]]
 * 