# AAA
#Just for study  
## Chapter 01  
 > >Problem 1:My conda environment got crushing while activate because of the losing of 'requests' module.  
 > >Solve:   
 >>pip install requests   
 >>conda init  
>>restart project  
> >Problem 2:When I tried to call the API of LLM,I failed because I didnt know the base_url of llm.  
> >Solve: Actually it has the course in official documents.  
>  >***Q1***:What are the difference between LLM & Agent?If give the same question to the LLM,what's the result?  
>  >**A1**:I believe the key difference between LLMS and Agents lies in whether they can make autonomous decisions.LLMs depend on their knowledge bases.LLMs may make things up when faced with questions beyond their knowledge base. This is because their knowledge base is inherently limited.Agents can utilize tools such as online search capabilities and time queries. However, offline LLMs typically cannot retrieve the latest weather or attraction information.  
>  >***Q2***:Deepseek can utilize tools such as online search capabilities,it that means deepseek is an agent?    
>  >**A2**:No.As I answered before,the key difference between LLMS and Agents lies in whether they can make autonomous decisions.Agents can decide to use tools(such as online search) autononously.Instead,LLMs decide to use tools by human not themselves because we push the button that actually we decide to use tools.Also,some workflows can use tools.Therefore，I believe that using the criterion of whether we can call upon the tools as the basis for differentiation is not entirely correct.   
**Where I get the API?**  
> >[id]:https://modelscope.cn/ "LLM"  
>  >**Where I get the dataAPI?**  
>  >[id]:https://app.tavily.com/ "data"
>  >
>  >## Chapter 02
>  >I try to understand what is 'transformer' and what is 'self-attention',but I still feel confused.  
>  >**# self attention**  
>  >A single pass through the 'self-attention mechanism' is insufficient to achieve a deep understanding of semantics.Because this mechanism can only establish a single connection between words.But in reality,a single word usually has multifaceted semantics.  
>  >**# Transformer**  
>  >In my view,'transformer' depends 'attention',it solves the problem like if a word has two propoerties,and the RNN can't distinguish the difference,and through a mechanism called 'self-attention',that it can do it.This is my understanding.And I just know this 'attention' is derived through matrix transformations and vector transformations, but I don't quite grasp the underlying principles.And I think the llm or agents not even truly understanding the natural language,they just train by lots of data and it generate by probability.  
>  >Transfomer uses 'MultiHeadAttention' to addrese the limitations of self-attention mechanisms.  
>  >**# self attention process**:  
>  >(1)Transformer uses Part-of-Speech tool to divide a sentence into pieces(the smallest meaning unit),that is token.  
>  >(2)Tokens are encoded into word vectors composed of 512-bit values. However, since these word vectors are parallel, positional encoding is added to indicate their sequence. Thus, the word vectors and positional encoding together form a word vector group.To understand the relationships between these words, we need to have them compute each other.  
>  >(3)To enable mutual computation, the model first multiplies each of the three weight matrices（W_K,W_Q,W_V) by each word vector group to obtain the corresponding Q, K, and V for each word vector group.  
>  >(4)Next, the model performs a dot product operation by multiplying the Q vector of each word with the K vectors of all words in the sentence, including the word itself.  
>  >(5)To make the scores appear reasonable, the computed results are typically divided by a constant (d_k), where d_k is the dimension of the vector, preventing gradient explosion. This yields a set of attention scores.  
>  >(6)Then,these scores are passed through a Softmax function, compressing them all between 0 and 1 to produce a set of attention weights. These weights represent the degree of association between the current word and other words.  
>  >(7)Last, multiply each word's V vector by its corresponding attention weight, then perform a weighted sum to obtain a new set of vectors. This new set of vectors will encompass every word in the sentence along with an understanding of the meanings of other words.  
>  >
>  >## Chapter 03
>  >

