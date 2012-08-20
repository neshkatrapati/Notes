Chapter 8 - Word Classes And POS Tagging
========================================

Introduction
------------

* Parts of speech
	* Equivalance classes
	* Gives significant information about the words	
* Recent Models of POS
	* Penn Treebank
	* Brown Corpus 
	* C7 tagset
* Applications
	* Useful for spech recognition
	* Useful for stemming and morph-analysis
	* IR/IE Systems
* Approaches
	* Rule Based
	* Stochastic
	* Transformational

English Word Classes
--------------------
* Traditional
	- Words grouped WRT **morphological properties** and WRT which words can occur nearby `(`**Distributional properties**`)`
* Words also have semantic coherence, but we don't generally consider that.
* Categories
	- Open Vs Closed
	- Closed can also be called **functional words**
	- Open Classes
		> Nouns, Verbs ,Adjectives, Adverbs
		> Lakhota a native american indian language dosen't have adjectives. They can be translated to verbs
* Nouns 
	- Ability to occur with **Determiniers**
	- Take possesives `(`Rama's,his`)`
	- Most of all, the plural form 
	- Proper Nouns 
		- Names, Entities 
		- Aren't preceded by articles
		- Ususaly Capitalized
	- Common Nouns 
		- Count Nouns 
			- Goat, Goats 
			- One goat, Two Goats
		- Mass noun 
			- Air, Water, Salt, Capitalism etc 
			- Can't be pluralized 
* Verbs 
	- Forms of the verbs `(`Morphological`)`
		* 3-p-Sg,3-p-Pl,Progressive(-ing),past participle(eaten)
* Adjectives
* Adverbs 
	- Directional or Locative
		* here,downhill,home
	- Degree
		* Extremely,Slowly,Delicately
	- Temporal 
		* yesterday, Monday etc
* Prepositions 
	- Temporal,Spatial,Literal or Metaphorical
	- Particles 
		* Resembles adverb or preposition and combines with a verb to form **phrasal verb**
* Articles
* Conjunctions 
	- Join two 
		* Phrases
		* Clauses
		* Sentences
	- Coordinating 
		* Join parts of same status 
		* and, but, or 
	- Subordinating 
		* Joins main class with subordinate class
		* ex : that.
	- Complementizer
		* "I thought that you would like a toast"
		* that combines with the verb thought. These are called complemetizers
* Pronouns 
	- Personal
	- Posessive
	- WH-Pronouns
* Auxillary verbs 
	- Suggest the Tense,Aspect,Modality
	- **Copula** Verbs "Be","Have"
		* Can be used as passive,progressive
		* Used to mark perfet senses etc
	- **Modal** verbs like can,shall,must indicate the mood

Tagsets for English
------------------
* Existing 
	- 45 - Penn Tree
	- 61 - C5 - CLAWS
	- 146 - C7 - BNC
	- Penn has less tags than C5 because it also involved parsing which clears ambiguities and makes some tags less nessecary
* Tagsets are to be seleced depending upon the information needed

POS Tagging
-----------
* Ambiguity
* ENGTWOL
* HMM Tagger
* Brills 

Rule Based Tagging 
----------------
* Two step approach 
	- Step 1 : Assign all possible tags to words `(`Using a dictionary`)`
	- Step 2: Narrow the tags using handmade rules
* __ENGTWOL__
	- 56,000 Entries 
		* Including noun forms,verb forms etc of every word seperately

Stochastic POS Tagging 
--------------------
* HMM Taggers
	- P(word|tag)*P(tag|previous n tags)
	- ti = argmaxP(tj|ti-1,wi)
		* Chooses the most probable tag i given previous tag i-1 and the current word 
	- Can be restated as 
		* ti = argmaxP(tj|ti-1)P(wi|tj)
			- The probablity of tag j occuring given prev tag X probablity of word i occuring for this tag.
	- Example 
		* The/Det race/NN to the witch mountain
			- P(NN|Det)*P(race|NN)
		* He has to/TO race/VB tomorrow 
			- P(VB|TO)*P(race|VB)

Transformation Tagging
--------------------
* Also Brills Tagging 
* Instance of Transformation based learning 
* Inspired from both, rule based and stochastic approaches
* Approach 
	- First tagged with broader rules. This gives many errors
	- Then a slightly more specific rule is selected which makes less errors and so on. 
	- Basic approach is like HMM. But, when the tag is mispredicted, the tagger learns the __Transformational Rule__
* Stages 
	- 3 Stages
		1. Label the word with most likely tag
		2. Selects a good transformational rule 
		3. Applies it.
* Templates 
	- Used to limit the number of transformations 
	- Every rule is an instance of templates
* 
 
Tagger Evaluation
---------------
* Human Gold Standard 
* Baselines and Ceilings
* Human Ceiling 
	- Check the %age of how much humans agree
* Human Baseline 
	- Compare against human baseline
			
	

	
