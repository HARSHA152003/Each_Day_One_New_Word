# Each_Day_One_New_Word

## Vocabulary quiz

The public quiz is available at `quiz.html` and reads words from the existing
Supabase `public.words` table. Run `quiz_import.sql` in the Supabase SQL
Editor to add quiz-only `quiz_meaning` and `quiz_sentence` columns and populate
them for matching existing words. The regular `meaning` column is preserved
for the vocabulary pages; quiz answer choices use the separate concise
`quiz_meaning` value. The import fills both quiz fields for the existing word
list.

Quiz setup defaults to the latest 10 dated words and also supports all words,
a date range, or a first-letter range. Fill-in-the-blank is an available quiz
style, but questions are only drawn from words that have a sentence entered by
faculty. Mixed style includes fill-in questions only when a sentence is
available for that word.

Faculty can add or edit a literal quiz meaning and quiz sentence in
`faculty.html`. Enter the complete sentence and use `[blank]` where the answer
belongs; the **Insert [blank] at cursor** button adds the marker. Existing
sentences with underscore markers remain supported.

The faculty page has separate Add, Today, Calendar, Download, Earlier, and
Quiz editor pages. Download is next to Earlier in the navigation. The quiz
preview/editor includes Today, Last 10, All words,
words missing either quiz field, available-date range, and first-letter range
filters. The date range uses calendar-style inputs constrained to the earliest
and latest dates with words. Quiz fields can also be reviewed alongside words
in the Today and
Calendar views; Earlier shows the meaning and example, while its edit action
still opens all editable fields. The quiz meaning is optional. The Download
page exports all loaded word data as JSON or as a UTF-8 CSV that opens in Excel.