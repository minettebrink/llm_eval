# Evaluation of Math LLM

I've prompt engineerd previously a Mistral Large 7B model to answer mathematical questions. Now I want to evaluate that model. 

I've used mathematics_dataset as a test dataset. Not the best choise because it is open source and there is a big possibility that Mistral has used that data set for training their models. But it'll do for know and work for this porpose to show my chain of thought. If I would actually want to test my Math LLM one option would be to create my own data set. 

So far I've tried 
- different smaller open source LLMs to compare the answer that Math LLM gives and to the correct answer in the data set.
    - The models where to unreliable and it was about a 50/50 chanse that they answered right. 
    - I prompt enginered the models but I did not fine tune the models. 
- I came to a conclusion that it is better to do an exact match of the final answer of the Math LLMs answer. 
    - The formatting is difficult, because it needs to match exactly the answer in the mathematics_dataset
    - It only compares the final answer. This means that the reasoning can be wrong in the answer of Math LLM even if the answer is correct.

Next step:
- Continue with the exact match 
- Try [Math Verify](https://github.com/huggingface/Math-Verify)