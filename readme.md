# Evaluation of Math LLM

I've previously prompt-engineered a Mistral Large 7B model to answer mathematical questions. Now, I want to evaluate the mathematical part of that model. 

I've used mathematics_dataset as a test dataset. It is not the best choice because it is open source, and it is a big possibility that Mistral has used that data set for training their models. But it'll do for now and work to show my chain of thought for this purpose. If I actually want to test my Math LLM, one option would be to create my own data set. 

So far, I've tried 
- Different smaller open-source LLMs are used to compare the answer that Math LLM gives to the correct answer in the data set.
    - The models were too unreliable, and there was about a 50/50 chance that they answered correctly. 
    - I prompt engineered the models but did not fine-tune the models. 
- I concluded that it is better to do an exact match of the final answer of the Math LLMs answer. 
    - The formatting is difficult because it needs to match precisely the answer in the mathematics_dataset
    - It only compares the final answer. This means that the reasoning for the answer to mathematical LLM can be wrong, even if the answer is correct.

Next step:
- Continue with the exact match 
- Try [Math Verify](https://github.com/huggingface/Math-Verify)