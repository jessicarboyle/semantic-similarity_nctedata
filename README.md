# Semantic Similarity of Teacher and Student Discourse Linked to Quality Ratings from Classroom Observations 
**Overview:**

Effective classroom communication is critical for students' academic performance. This study investigates the semantic similarity of adjacent teacher-to-student, teacher-to-teacher, and student-to-student utterances using natural language processing (NLP) tools. It explores their relationship with quality ratings of Instructional Dialogue obtained from Classroom Atmosphere Scoring System (CLASS) observations and the quality ratings of Teacher’s Use of Student Contribution from Mathematical Quality of Instruction (MQI) observations. Focusing on the cohesiveness of classroom language, the study analyzes transcripts from elementary math classrooms, associating each with corresponding CLASS scores. Linear regression models identified that the semantic similarity between teacher-to-student utterances was a significant predictor of the CLASS and MQI scores. However, the models explain little variance in the observational scores. The study underscores the complexity of classroom discourse and proposes future analyses. Additionally, it explores the utility of NLP tools in measuring teacher practices, emphasizing the need for advancements in audio and textual models trained on speech-to-text transcriptions for accurate spoken language analysis. The findings prompt reflection on the practical significance of observed associations and highlight the importance of considering the evolving landscape of educational technology in supporting teacher practice.

To assess the cohesiveness of teachers and student discourse, spaCy was used to calculate the semantic similarity between adjacent teacher-to-student utterances, adjacent teacher-to-teacher utterances, and adjacent student-to-student utterances. This was completed for all words included in the transcripts and exclusively for the content words in each utterance. This analysis examines the teacher-to-student, teacher-to-teacher, and student-to-student utterances’ semantic similarity and their relation to the quality ratings for Instructional Dialogue CLASS scores and teacher-to-student semantic similarity to the Teacher Use of Student Contribution MQI scores.

**Data:**

The open-source National Center for Teacher Effectiveness (NCTE) transcript dataset includes anonymized transcripts from teachers’ classroom observations from the NCTE Main Study [20]. The observations occurred between 2010-2013 in 4th and 5th-grade elementary math classrooms across four dis-tricts, predominately serving historically marginalized stu-dents. The transcripts are linked with a variety of outcome variables including classroom observation scores, demograph-ic information, survey responses, and student scores. The en-tire NCTE dataset can be found at: https://github.com/ddemszky/classroom-transcript-analysis. This analysis focused on the classroom transcripts and the linked Classroom Atmosphere Scoring System (CLASS) data. 

**Classroom Transcripts

This analysis includes 1325 observation transcripts from 301 teachers, each with an average of 4 transcripts. Classroom les-sons were captured using three cameras, a lapel microphone for teacher talk, and a bidirectional microphone for student talk. The recordings were transcribed by professional transcribers working under contract for a commercial transcription compa-ny. 
The transcripts were organized by speaker turns (teacher, stu-dents, multiple students) where each row of the transcript data frame represents a speaker turn or utterance that may contain one or more speech acts or "sentences". In this analysis, stu-dent talk was removed and only teacher turns were analyzed. On average, the transcripts contain 5,733 words, with 87.7% of which are spoken by the teachers, and with 172 teacher ut-terances per transcript.
The transcripts are fully anonymized: student and teacher names are replaced with terms like “Student J”, “Teacher” or “Mrs. H”. Transcribers used square brackets to indicate when speech was [Inaudible], if they were unsure of a particular word due to audio quality, or to include meta-data such as [laughter], [students putting away materials]. All bracketed information was removed from the transcripts for this analy-sis. 


**Classroom Assessment Scoring System (CLASS) Scores

The CLASS is an observation tool used to assess the quality of teacher-student interactions across 3 broad domains: emotional support, classroom organization, and instructional support. The 3 domains include a total of 11 sub-dimensions. This analysis includes the Instructional Dialogue dimension from the Instructional Support domain. Observers score each dimension using a 7-point scale.

**Mathematical Quality of Instruction (MQI)

The Mathematical Quality of Instruction (MQI) instrument is used to measure the quality of math instruction across five elements: richness of the mathematics; errors and imprecision; working with students and mathematics; student participation in meaning-making and reasoning; and connections between classroom work and mathematics. This analysis includes the Teacher’s Use of Student Contribution scores from the working with students and mathematics element. Observers scored each item using a 4-point scale.


**Code Included:**

**.ipyn file

This codes includes data cleaning and the semantic similarity analysis. The analysis of semantic similarity aimed to assess the cohesion of teacher and student discourse by calculating the similarity between adjacent utterances. Two distinct analyses were conducted to provide a richer understanding of semantic similarity: one considering all words and the other focusing solely on content words. The semantic similarity was computed for teacher-to-student utterances, only teacher-to-teacher utterances (removed student utterances), and only student-to-student utterances (removed teacher utterances).

**.rmd files

This code includes the statistical analysis examining the relationship between semantic similarity scores and the CLASS & MQI measures. It includes examining correlations and 10-fold cross validation linear regression models. 




