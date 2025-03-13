# Mini_Project_KIIT
## Srinjoy Sengupta
## B.Tech ( C.S.E)
## Mini Project Sixth Semester
## Kalinga Institute of Industrial Technology (KIIT), Odisha, India
#### Explanation of Word Mover's Distance
Imagine you have a box of different colored LEGO blocks, and each color represents a word. Now, let's say you want to build two towers out of these blocks, but the towers look a little different from each other.

The **Word Mover's Distance (WMD)** is like figuring out the smallest number of steps it would take to move the blocks around so that one tower looks exactly like the other one. In this case, the blocks are words, and the steps are how different the words are from each other.

For example, if one tower has a red block (representing the word "cat") and the other has a pink block (representing the word "kitten"), it wouldn't take many steps to swap them because they’re pretty similar. But if it was a red block ("cat") and a blue block ("car"), it would take more steps since those words are less related.

The WMD algorithm does this for all the words in two sentences to see how "close" the meanings of the sentences are. If it takes just a few steps, the sentences mean almost the same thing. If it takes a lot of steps, the meanings are quite different.
#### Explanation of Optimised Word Mover's Distance Algorithm
Imagine again that you have those LEGO towers, but now, you’re smarter about which blocks to move.

Let’s say some blocks have special stickers on them—like “NOUN” or “VERB”—to show what type of word they are, like naming things (NOUN, like “cat” or “dog”) or actions (VERB, like “run” or “jump”). You realize that some blocks are more important for building the tower’s shape than others.

For example, in the sentence “The cat is jumping,” the important words are “cat” (a NOUN) and “jumping” (a VERB). Words like “the” and “is” are like tiny connector blocks that don’t change the tower’s shape much.

So, in the **optimized Word Mover’s Distance (WMD)**, you decide to:
1. Focus mainly on the important blocks with stickers like NOUN (NN, NNS), VERB (VBG, VBZ), and ADJECTIVE (JJ).
2. Ignore or give less importance to tiny connector blocks like “the,” “is,” or “and” because they don’t change the meaning much.

By being picky about which blocks to move, you need fewer steps to make the towers look the same, and you get the answer faster! This is how the optimized version makes comparing sentence meanings quicker and more accurate.
### Word Mover Distance Algorithm in Bengali Language
FastText helps implement Word Mover's Distance (WMD) in Bengali by providing word embeddings that capture both the meaning and structure of words, even for rare or out-of-vocabulary terms. Unlike traditional word embeddings, FastText represents words as character n-grams, which is especially useful for Bengali due to its complex morphology and word variations. This ability to generate meaningful embeddings for a wide range of words makes it an ideal choice for calculating WMD in Bengali, allowing for more accurate text comparisons based on semantic similarity.
### **Optimized Word Mover’s Distance (OWMD) on Bengali Text Using POS Tag-Based Classification**

<p align="justify">
Optimized Word Mover’s Distance (OWMD) is a refined version of Word Mover’s Distance (WMD) that improves similarity measurement between two text samples. In our approach, we apply OWMD to Bengali text by first performing tokenization and Part-of-Speech (POS) tagging using a Bengali POS tagger. To enhance accuracy, we classify words based on their POS tags, selecting <b>nouns (NN), verbs (VM), adjectives (JJ), and adverbs (RB)</b> as relevant words for similarity computation. If no such words exist, we fall back to using all tokens to avoid empty inputs that cause infinite distance values. We then compute the Word Mover’s Distance (WMD) using FastText word embeddings, followed by converting it into <b>Optimized Word Mover’s Similarity (OWMS) using an exponential function</b>. This process ensures a robust semantic similarity measurement, effectively handling Bengali linguistic structures while mitigating errors due to insufficient content-bearing words.
</p>
