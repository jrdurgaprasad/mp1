# MP1 Prompt Lab -- Compare LLM Strategies 

|  |  |
|---|---|
| Author | J R Durgaprasad |
| Email | jr.durgaprasad@gmail.com |
| Github Link | https://github.com/jrdurgaprasad/mp1.git |
| Branch to pull | master |
|  |  |

## Project Context

The usecase provide with different job snippets in .jsonl file along with expected golden dataset to be derive, compare and compute the comparision scores with different prompting strategies.

## Objective

A small notebook or script that compares the below four prompting strategies on the same task and tells us which one wins with numbers not by opinions for the context given.

## Project Structure

The mini project contains the following file hierarchy:

```text
mp1/
├── README.md
├── requirements.txt
├── mp1_prompt_lab.ipynb
├── mp1_comparison.md
└── mp1_writeup.md
```

## Instructions to Run the Notebook

1. Open a terminal in the project folder:

   ```bash
   cd /voc/work/mp1
   ```

2. Check the python version installed in the terminal is having >=3.10.x, 
   ``` bash
   python --version
   ````

    If python not installed or not available, please install before proceeding with next steps.

3. Create and activate a Python virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. Install the required dependencies in the virtual environment:

   ```bash
   pip install -r requirements.txt
   ```
4. Copy the folder 'data/' containing job_snippets.jsonl and golden_set.jsonl to local folder either inside the directory 'mp1/' or outside.
5. Start Jupyter Notebook:

   ```bash
   jupyter notebook mp1_prompt_lab.ipynb
   ```

   Alternatively, open the notebook in VS Code or vocareum and select the environment created above as the kernel.

5. Copy the folder 'data/' containing job_snippets.jsonl and golden_set.jsonl from https://classroom.emeritus.org by following below steps:
   Select Modules --> Week 5: Graded Mini Project --> under Submission Guidelines section --> click on '**Week 5_Graded Mini Project Documents**' to download.
   Unzip the downloaded folder and traverse through Week 5_Graded Mini Project 'Documents.zip\AI-RAG_MP1_PromptLab\MP1_PromptLab\data directory' to get above .jsonl files.

7. The print statement in the notebook mp1_prompt_lab.ipynb cell 2 is not printing OPENAI_API_KEY, replace your OpenAI API KEY in following python statement and copy and paste in the cell 3 line 1.

   ```python
   client = AsyncOpenAI(
      api_key=os.environ.get('OPENAI_API_KEY','<your OpenAI API Key>'),
      base_url='https://openai.vocareum.com/v1'
   )
   ```
   Also, in the cell 4 change the path mentioned in the first line while assigning 'data/' path to DIR_PATH varaible accordingly based on the 'data/' directory local path.
   ```python
   DATA_DIR = Path('./data')
   # OR
   DATA_DIR = Path('../data') 
   ```
   
   #### Note: This helps us to run the same code in local code editors like VS Code etc with same enviornment configuration mention in steps 1 - 5.

8. Run the notebook cells from top to bottom either one after another or all at once.
