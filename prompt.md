# ESL Bilingual Worksheet Generator v1.8
🧠 Created by Abner Carvalho – github.com/Johnny-armless

This prompt generates **two customized ESL worksheets**:
- 🎓 `Student Worksheet` (exercises only)
- 🧑‍🏫 `Teacher Worksheet` (with answers + explanations + ElevenLabs guide)

---

## ▶️ Prompt (copy and paste into ChatGPT)

!INIT[esl_bilingual_worksheet_v1.8]

→ QUERY[instruction_lang] :: Ask: "What is the student’s native language?"
→ STORE → $instruction_lang

→ QUERY[exercise_lang] :: Ask: "What is the target language of the exercises?"
→ STORE → $exercise_lang

→ QUERY[cefr_level] :: Ask: "What is the CEFR level of the student? (A1–C2)"
→ STORE → $cefr_level

→ QUERY[focus_topics] :: Ask: "Which topics should be included?"
→ STORE → $focus_topics

→ QUERY[avoid_topics] :: Ask: "Are there any topics to avoid?"
→ STORE → $avoid_topics

→ QUERY[grammar_point] :: Ask: "Which grammar point should be the focus?"
→ STORE → $grammar_point

→ PROCESS:
  ⤷ GEN_TwoDocuments($instruction_lang, $exercise_lang, $cefr_level, $focus_topics, $avoid_topics, $grammar_point)

→ FORMAT: 2 DOCX files
  - 📄 `ESL_Worksheet_Student_by_Abner.docx` (clean worksheet)
  - 📘 `ESL_Worksheet_Teacher_by_Abner.docx` (with answers and guides)

---

## 🧾 Content Structure

**All section titles and instructions are shown in the student’s native language.**

1. **(Warm-up)** → One simple question related to the topic.
2. **(Grammar Explanation)** → In native language; examples in exercise language.
3. **(Sentence Builder)** → Write sentences using word groups (4 sets).  
   ✅ Teacher doc includes model answers.
4. **(Match the Columns)** → Displayed as a two-column table.  
   ✅ Teacher doc includes correct matches.
5. **(Fill in the Gaps)** → 4 short sentences with blanks.  
   ✅ Teacher doc includes correct answers.
6. **(Sentence Transformation)** → 5 sentences to change (affirmative ↔ negative/interrogative).  
   ✅ Teacher doc includes all transformed forms.
7. **(Dictation)**  
   - Instructions in native language.  
   - 10-word list with IPA.  
   - ElevenLabs guide: “Say word → wait 5s → repeat → wait 5s → next.”
   ✅ Teacher doc includes correct spellings and verb list for ElevenLabs.

---

## ✅ Teacher File Extras

- CEFR level and grammar/topic metadata
- Explanation of how to use ElevenLabs.com for recording dictation
- Answer key for all sections

---

## 👤 Credits

**Prompt developed by Abner Carvalho**  
**Supernova English School** – [github.com/Johnny-armless](https://github.com/Johnny-armless)

“This worksheet was generated using AI to support your ESL classroom.”