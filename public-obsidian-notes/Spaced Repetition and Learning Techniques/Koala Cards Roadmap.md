### Problems
- Need a "Refresh" button for incorrect card illustrations, such as the card "Await the order".
- It's too hard to edit cards when I spot an error mid review
#### Small Features
- Integrate PostHog to see usage patterns and get feedback
- Add notes
	- Make similar cards
	- Refresh definition
	- Double check card meaning/definition
	- Change tense
- Force 100% recitation of failed cards in same session.
- Add a "refresh" button to the final page of the "Add Cards" flow for when it doesn't come out quite right.
- Include the card front/back when sending transcription to Whisper (might reduce transcription error rate).
### Experiments

 - Hire someone to label data for fine tuning (SEE: Soomgo)
 - Do preference based fine tuning for grammar corrections: https://platform.openai.com/docs/guides/fine-tuning#preference
 - On the final page, create a "Download Summary" button that creates a downloadable HTML file that can be emailed to tutors.
	 - Bigger experiment: Auto-expiring review summary page
 - Replace Google Cloud TTS with [Replicate/xTTS](https://replicate.com/lucataco/xtts-v2)
 - Example generator: Definition Quiz => Create Card for unknown/missed words
### Routine Features
 * Once there are no more cards for review, transition to "cram mode" which reviews cards in difficulty order and does typing / speaking tests with no grading.
 * Decks
 * Shared Decks
 * Ability to attach notes to cards
 * New Card types
	 * Image identification (for nouns)
	 * Listening / reading comprehension (theme + vocabulary word = machine generated paragraph and followup questions)
	 * Typing (a dictation test for spelling)
	 * Speaking scenarios and conversation prompts.
 * Learning session options (listening only, one deck only, one language only, etc)
 * Card progression (dictation => Reading => Listening => Speaking)
 * FSRS Revlog
 * Card notes that are shown/added on failure.
### Crazy Ideas

 * [[Situation and Goal Language Drills]]
- Vectorize all feedback, perform clustering, create a list of improvement goals.
- Add a Beeminder integration
- Dual-N-Back paragraph comprehension exercise
 * Ability for students to link teachers or tutors to their account.
	 * Share top N most difficult cards
	 * Voice recording submission to teacher for pronunciation feedback
### Koala Cards
 * [[Koala Cards Roadmap]]