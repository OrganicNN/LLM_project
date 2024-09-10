# LLM_project
 Through this project, I am learning to gain experience with LLMs. 
Upon seeking to get started in LLMs, I came across [this github repo](https://github.com/Hannibal046/Awesome-LLM) along with many other links from the New Stack blog, Medium and Wikipedia! 

Personally, I want to use open source and gain applied engineering experience of deploying an app end-to-end. Hence, to start, I understood 2 things:
1. Ollama - This will allow me to run open source LLMs locally.
2. LangChain - This will give me a framework to develop an LLM app.

Using google's colab and Analytics Vidhya's courses, I created [this](https://github.com/OrganicNN/LLM_project/blob/main/Prompt_engineering_using_ollama_llama3_1.ipynb) notebook to learn about prompt engineering.
There, we can explore various LLMs (in the notebook I have used llama3.1 but can use mistral or another offered by ollama (depending on what your google colab can handle))

On my local machine, I wish to use jupyter notebooks for coding and development under conda virtual environment.
The following instructions are for getting started on your local machine. 

---

The following commands were run in the Anaconda3 Prompt in a virtual environment

Installing Ollama: 
```
conda install conda-forge::ollama
conda pull llama2
```
Note that instead of `llama2`, another Open LLM models can be used such as Mistral, etc.
Once llama is pulled, we need to start:

`ollama serve`

Then check http://localhost:11434/ in your browser to see if you get a message saying, "Ollama is running".
Test it out in command prompt - Note this will be very very noisy:
```
⠸ ←[?25h←[?25l←[2K←[1G⠼ ←[?25h←[?25l←[2K←[1G⠴ ←[?25h←[?25l←[2K←[1G⠦ ←[?25h←[?25l←[2K←[1G⠧ ←[?25h←[?25l←[2K←[1G⠇ ←[?25h←[?25l←[2K←[1G⠏ ←[?25h←[?25l←[2K←[1G⠋ ←[?25h←[?25l←[2K←[1G⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[2K←[1G⠸ ←[?25h←[?25l←[?25l←[2K←[1G←[?25h←[2K←[1G←[?25h←[?25l←[?25h←[?2004h>>> ←[38;5;245mSend a message (/? for help)←[28D←[0m "Tell me a joke"
←[K "Tell me a joke"
←[?25l⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[2K←[1G⠸ ←[?25h←[?25l←[2K←[1G⠼ ←[?25h←[?25l←[2K←[1G⠴ ←[?25h←[?25l←[2K←[1G⠦ ←[?25h←[?25l←[2K←[1G⠧ ←[?25h←[?25l←[2K←[1G⠇ ←[?25h←[?25l←[2K←[1G⠏ ←[?25h←[?25l←[2K←[1G⠋ ←[?25h←[?25l←[2K←[1G⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[2K←[1G⠸ ←[?25h←[?25l←[2K←[1G⠼ ←[?25h←[?25l←[2K←[1G⠴ ←[?25h←[?25l←[2K←[1G⠦ ←[?25h←[?25l←[2K←[1G⠧ ←[?25h←[?25l←[2K←[1G⠇ ←[?25h←[?25l←[2K←[1G⠏ ←[?25h←[?25l←[2K←[1G⠋ ←[?25h←[?25l←[2K←[1G⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[2K←[1G⠸ ←[?25h←[?25l←[2K←[1G⠼ ←[?25h←[?25l←[2K←[1G⠴ ←[?25h←[?25l←[2K←[1G⠦ ←[?25h←[?25l←[2K←[1G⠧ ←[?25h←[?25l←[2K←[1G⠇ ←[?25h←[?25l←[2K←[1G⠏ ←[?25h←[?25l←[2K←[1G⠋ ←[?25h←[?25l←[2K←[1G⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[2K←[1G⠸ ←[?25h←[?25l←[2K←[1G⠼ ←[?25h←[?25l←[2K←[1G⠴ ←[?25h←[?25l←[2K←[1G⠦ ←[?25h←[?25l←[2K←[1G⠧ ←[?25h←[?25l←[2K←[1G⠇ ←[?25h←[?25l←[2K←[1G⠏ ←[?25h←[?25l←[2K←[1G⠋ ←[?25h←[?25l←[2K←[1G⠙ ←[?25h←[?25l←[2K←[1G⠹ ←[?25h←[?25l←[?25l←[2K←[1G←[?25h←[2K←[1G←[?25h
←[?25l←[?25hS←[?25l←[?25hure←[?25l←[?25h!←[?25l←[?25h Here←[?25l←[?25h'←[?25l←[?25hs←[?25l←[?25h a←[?25l←[?25h short←[?25l←[?25h and←[?25l←[?25h simple←[?25l←[?25h jo←[?25l←[?25hke←[?25l←[?25h:←[?25l←[?25h
←[?25l←[?25h
←[?25l←[?25hWhy←[?25l←[?25h don←[?25l←[?25h'←[?25l←[?25ht←[?25l←[?25h scient←[?25l←[?25hists←[?25l←[?25h trust←[?25l←[?25h atoms←[?25l←[?25h?←[?25l←[?25h
←[?25l←[?25hB←[?25l←[?25hecause←[?25l←[?25h they←[?25l←[?25h make←[?25l←[?25h up←[?25l←[?25h everything←[?25l←[?25h!←[?25l←[?25h
←[?25l←[?25h
←[?25l←[?25hI←[?25l←[?25h hope←[?25l←[?25h that←[?25l←[?25h brought←[?25l←[?25h a←[?25l←[?25h smile←[?25l←[?25h to←[?25l←[?25h your←[?25l←[?25h face←[?25l←[?25h!←[?25l←[?25h Do←[?25l←[?25h you←[?25l←[?25h want←[?25l←[?25h to←[?25l←[?25h hear←[?25l←[?25h another←[?25l←[?25h one←[?25l←[?25h?←[?25l←[?25h

←[?25l←[?25h>>> ←[38;5;245mSend a message (/? for help)←[28D←[0m←[K←[38;5;245mSend a message (/? for help)←[28D←[0m←[K
←[?2004l

```

>Note that the prompt was: "Tell me a joke" and the corresponding response was:
>>"Sure, here's a classic one:
>>
>>Why don't scientists trust atoms?
>>
>>Because they make up everything!
>>
>>I hope that made you smile!"

---

Next, let us try getting a cleaner response and get out of prompt and into jupyter notebook. For this, we will install LangChain. In the prompt,
```
conda install conda-forge::langchain
pip install langchain-community langchain-core
```
With this, we are set to run the notebook.
Run `ollama serve` on the command line, check http://localhost:11434/ in your browser to see if you get a message saying, "Ollama is running".  
Then, fire up the notebook, "LLM_trial.ipynb" from this repo.

To be continued.
