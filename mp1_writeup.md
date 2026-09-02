# 1. Which strategy won, and on what dimension? (Accuracy? Parse rate? Cost?)

Few shots and Structured won with respect to accuracy and judge score combainly. It should be because we are providing structured prompt with more context and expamples for the results expected or to be predicted.

I rewritten the structured prompt several times to improve accuracy upto 2.8 from 2.0. After providing a sample/example snippet and output JSON, the accuracy reached to 2.8.

# 2. What surprised you? Either a strategy worked better than expected, or worse, or a specific snippet failed in a way you didn't predict.

Zero-shot strategy gave the results same judge score as structured prompt with low latency or processing time. This prove me wrong that without examples it gave decent accuracy 2.6.

# 3. For *Learner Guide* capstone domain, which strategy would you reach for first? Justify in 2-3 sentences.
My first choice would be Structured prompt + few shots pattern because it will be more accurate when combaining Structured promot with few examples. This also reduces the LLM response latency for the end user.

# 4. If you had another day, what would you try next? (Different model? More snippets? Different prompts?)

I will try to improve the CoT prompt pattern to improve the accuracy and it can helps me to reduce latency as well. So that it may help me to decide the prompt strategy to chose in my capstone project.

Also, I would prepare larger size of input snippet and try with given model along with claude or gemeni flash models.

I will also try to add ADR document as well.

