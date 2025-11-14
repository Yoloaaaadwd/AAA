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
>  >#Transformer
>  >In my view,'transformer' depends 'attention',it solves the problem like if a word has two propoerties,and the RNN can't distinguish the difference,and through a mechanism called 'self-attention',that it can do it.This is my understanding.And I just know this 'attention' is derived through matrix transformations and vector transformations, but I don't quite grasp the underlying principles.And I think the llm or agents not even truly understanding the natural language,they just train by lots of data and it generate by probability.
>  >
>  >## Chapter 03
>  >

