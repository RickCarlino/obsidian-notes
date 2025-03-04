### Problems
- It's too hard to edit cards when I spot an error mid review

#### Big Features

 - Koala Writer - A text editor for writing practice.
 - Reading comprehension quizzes
#### Small Features
- Integrate PostHog to see usage patterns and get feedback
- Save last failure explanation so you can read it on review.
- Add notes
	- Refresh definition
	- Double check card meaning/definition
	- Change tense
- Add a "refresh" button to the final page of the "Add Cards" flow for when it doesn't come out quite right.
- Need a "Refresh" button for incorrect card illustrations, such as the card "Await the order".
- Record dictation failures to identify hard to pronounce words.
- 
### Experiments

 - A public page where users can try speaking drills without authenticating. Just drills nothing else.
	 - Use this data set: https://tatoeba.org/en/downloads
 - Do preference based fine tuning for grammar corrections: https://platform.openai.com/docs/guides/fine-tuning#preference
 - On the final page, create a "Download Summary" button that creates a downloadable HTML file that can be emailed to tutors.
	 - Bigger experiment: Auto-expiring review summary page
 - Replace Google Cloud TTS with [Replicate/xTTS](https://replicate.com/lucataco/xtts-v2)or DeepGram (more likely)
 - Example generator: Definition Quiz => Create Card for unknown/missed words
### Routine Features
 * Once there are no more cards for review, transition to "cram mode" which reviews cards in difficulty order and does typing / speaking tests with no grading.

 * Shared Decks
 * Ability to attach notes to cards
 * New Card types
	 * Image identification (for nouns)
	 * Listening / reading comprehension (theme + vocabulary word = machine generated paragraph and followup questions)
	 * Typing (a dictation test for spelling)
	 * Speaking scenarios and conversation prompts.
 * Learning session options (listening only, ~~one deck only, one language only, etc~~)
 * ~~Card progression (dictation => Reading => Listening => Speaking)~~
 * FSRS Revlog
 * Card notes that are shown/added on failure.
### Crazy Ideas

 * [[Situation and Goal Language Drills]]
- Vectorize all feedback, perform clustering, create a list of improvement goals.
- Run stemming (via google cloud) on all cards and track student vocab knowledge.
	- Makes it possible to do i+1 style sentence progressions.
- Add a Beeminder integration
- Dual-N-Back paragraph comprehension exercise
 * Ability for students to link teachers or tutors to their account.
	 * Share top N most difficult cards
	 * Voice recording submission to teacher for pronunciation feedback

### Done

 * ~~Decks~~
 *  - 	- ~~Make similar cards~~
	- - ~~Force 100% recitation of failed cards in same session.~~
- ~~Include the card front/back when sending transcription to Whisper (might reduce transcription error rate).~~

 - ~~Hire someone to label data for fine tuning (SEE: Soomgo)~~
	 - Not needed after prompt refactor

