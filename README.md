# LLM-Projects
Repository for projects done to learn LLM engineering
![image](./Destination.JPG)

I'm so happy you're joining me on this path. We'll be building immensely satisfying projects in the coming weeks. Some will be easy, some will be challenging, many will ASTOUND you! The projects build on each other so you develop deeper and deeper expertise each week. One thing's for sure: you're going to have a lot of fun along the way.

# Before you begin
I'm here to help you be most successful with your learning! If you hit any snafus, or if you have any ideas on how I can improve the course, please do reach out in the platform or by emailing me direct (maadabushi@gmail.com). It's always great to connect with people on LinkedIn to build up the community - you'll find me here:
www.linkedin.com/in/sunil-m-072a8341
# Instant Gratification instructions with Llama 3.2 not Llama 3.3!
## Important note: see my warning about Llama3.3 below - it's too large for home computers! Stick with llama3.2! Seome may miss this warning...
We will start the course by installing Ollama so you can see results immediately!

Download and install Ollama from https://ollama.com noting that on a PC you might need to have administrator permissions for the install to work properly
On a PC, start a Command prompt / Powershell (Press Win + R, type cmd, and press Enter). On a Mac, start a Terminal (Applications > Utilities > Terminal).
Run ollama run llama3.2 or for smaller machines try ollama run llama3.2:1b - please note steer clear of Meta's latest model llama3.3 because at 70B parameters that's way too large for most home computers!
If this doesn't work: you may need to run ollama serve in another Powershell (Windows) or Terminal (Mac), and try step 3 again. On a PC, you may need to be running in an Admin instance of Powershell.
And if that doesn't work on your box, I've set up this on the cloud. This is on Google Colab, which will need you to have a Google account to sign in, but is free: https://colab.research.google.com/drive/1-_f5XZPsChvfU1sJ0QqCePtIuc55LSdu?usp=sharing
Any problems, please contact me!

# Then, Setup instructions
After we do the Ollama quick project, and after I introduce myself and the course, we get to work with the full environment setup.

Hopefully I've done a decent job of making these guides bulletproof - but please contact me right away if you hit roadblocks:

PC people please follow the instructions in SETUP-PC.md
Mac people please follow the instructions in SETUP-mac.md
Linux people please follow the instructions in SETUP-linux.md

# An important point on API costs (which are optional! No need to spend if you don't wish)
During the course, I'll suggest you try out the leading models at the forefront of progress, known as the Frontier models. I'll also suggest you run open-source models using Google Colab. These services have some charges, but I'll keep cost minimal - like, a few cents at a time. And I'll provide alternatives if you'd prefer not to use them.

Please do monitor your API usage to ensure you're comfortable with spend; I've included links below. There's no need to spend anything more than a couple of dollars for the entire course. Some AI providers such as OpenAI require a minimum credit like $5 or local equivalent; we should only spend a fraction of it, and you'll have plenty of opportunity to put it to good use in your own projects. During Week 7 you have an option to spend a bit more if you're enjoying the process - I spend about $10 myself and the results make me very happy indeed! But it's not necessary in the least; the important part is that you focus on learning.

# Free alternative to Paid APIs
Early in the course, I show you an alternative if you'd rather not spend anything on APIs:
Any time that we have code like:
openai = OpenAI()
You can use this as a direct replacement:
openai = OpenAI(base_url='http://localhost:11434/v1', api_key='ollama')
And also replace model names like gpt-4o-mini with llama3.2.
For week 1 day 1, you can find this in week1/solutions/day1_with_ollama.ipynb.

Below is a full example:

# You need to do this one time on your computer
!ollama pull llama3.2

from openai import OpenAI
MODEL = "llama3.2"
openai = OpenAI(base_url="http://localhost:11434/v1", api_key="ollama")

response = openai.chat.completions.create(
 model=MODEL,
 messages=[{"role": "user", "content": "What is 2 + 2?"}]
)

print(response.choices[0].message.content)

# How this Repo is organized
There are folders for each of the "weeks", representing the different, culminating in a powerful autonomous Agentic AI solution in Week 8 that draws on many of the prior weeks.
Follow the setup instructions above, then open the Week 1 folder and prepare for joy

# The most important part
The mantra of the course is: the best way to learn is by DOING. I don't type all the code during the course; I execute it for you to see the results. You should work along with me or after each lecture, running each cell, inspecting the objects to get a detailed understanding of what's happening. Then tweak the code and make it your own. There are juicy challenges for you throughout the course. I'd love it if you wanted to submit a Pull Request for your code (instructions here) and I can make your solutions available to others so we share in your progress; as an added benefit, you'll be recognized in GitHub for your contribution to the repo. While the projects are enjoyable, they are first and foremost designed to be educational, teaching you business skills that can be put into practice in your work.

# starting in Week 3, one can run Google Colab for running with GPUs
You should be able to use the free tier or minimal spend to complete all the projects in the class.

Learn about Google Colab and set up a Google account (if you don't already have one) here

The colab links are in the Week folders and also here:

For week 3 day 1, this Google Colab shows what colab can do
For week 3 day 2, here is a colab for the HuggingFace pipelines API
For week 3 day 3, here's the colab on Tokenizers
For week 3 day 4, we go to a colab with HuggingFace models
For week 3 day 5, we return to colab to make our Meeting Minutes product
For week 7, we will use these Colab books: Day 1 | Day 2 | Days 3 and 4 | Day 5

# Monitoring API charges
You can keep your API spend very low throughout this course; you can monitor spend at the dashboards: here for OpenAI, here for Anthropic and here for Google Gemini.

The charges for the exercsies in this course should always be quite low, but if you'd prefer to keep them minimal, then be sure to always choose the cheapest versions of models:

For OpenAI: Always use model gpt-4o-mini in the code instead of gpt-4o
For Anthropic: Always use model claude-3-haiku-20240307 in the code instead of the other Claude models
During week 7, look out for my instructions for using the cheaper dataset

Please do message me or email me at maadabushi@gmail.com if this doesn't work or if I can help with anything. I can't wait to hear how you get on.

