---
type: artikel
source: https://www.linkedin.com/posts/vsingh3_watson-won-jeopardy-so-how-come-it-didnt-ugcPost-7030181705936224256-29Zd?utm_source=share&utm_medium=member_ios
tags: [it, ai]
---

Watson won Jeopardy, so how come it didn't get us a great chatbot before ChatGPT? A lesson for tech leaders 

This is a question many puzzle over. Watson is hurriedly discarded as pure marketing and that misses the point. The reality is that Watson picked the wrong branch in the machine learning tree, and ended up in a dead end. 

IBM scientists were an ambitious bunch. In 1997, their invention Deep Blue beat Kasparov, & then Watson, an open domain Q & A system, beat Jennings in 2011. They seemed to have a big lead in artificial intelligence. 

However, a look underneath the hood shows that most techniques leveraged by Watson were on another branch of AI - a branch that emphasized rules. One such rules based technique was [[Slot grammar]] . This method encodes grammar rules into Watson's interpretation engine. This allowed Watson to unpack queries. Watson scientists also took knowledge, and structured it such that enabled easier traversal and retrieval. While this proved to be powerful, it was obviously unscalable. 

Getting Jeopardy like performance required large teams to encode new language patterns as rules, and curate all knowledge before Watson could do anything useful. This proved to be a Herculean task when Watson tried to take on health, and it eventually bombed. 

On the other hand, the branch that ChatGPT comes from is a branch that practically ignored any formalism of grammar, and chose to let the computer represent words as mathematical vectors. Once you store them as vectors, you can do algebra on words. 

Ironically, in 1997 when Deep Blue beat Kasparov, some scientists on a separate branch of ML published a now-revolutionary paper titled "LONG SHORT-TERM MEMORY". [[LSTM _ Introduction to LSTM _ Long Short Term Memory]]

The deep learning community continued to pursue this direction of words as vectors, and invented word embeddings in 2003 (by Bengio et Al). As computational power increased, this technique of letting a machine do mathematical operations on words continued to scale beautifully. In 2013 , google invented Pretrained word embeddings (word2vec). This was followed by attention models - which taught the machine which words to focus on in a sequence of words building upon the work done by the current Chief Scientist of OpenAI. In 2017, Transformer architecture was introduced by Google (by a scientist who was eventually lead on GPT) which enabled faster training of large language models. The rest is history. 

Today, most conversational systems are still largely based on what Watson incorporated. Rules based, requiring large human effort to get going, a lot of pre-work -- and ultimate collapse. They demo very well in confined settings and fall under their weight eventually. 

Conversational systems based on LLMs on the other hand are designed for scale, and do not require heavy human effort to make them work for each use case. 

The lesson here for tech leaders is to be careful about which branch of AI they are choosing.

[[Generatieve AI]]
[[LONG SHORT-TERM MEMORY]]
