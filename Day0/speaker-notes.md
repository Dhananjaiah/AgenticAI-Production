# Day 0 — simple read-aloud transcript

This script uses simple, everyday English. Read the normal paragraphs aloud. Text in **[square brackets]** tells you what to do and should not be read aloud.

Before recording, hide every real API key and private account detail. Use this transcript on a second screen, or press **N** in the presentation to see the same words.

Speak slowly, pause after new ideas, and show the real result from your computer before moving forward.


## 01. Get ready to buildproduction-minded AI.

[SLIDE 01 — Start here.]

Welcome to Day Zero.

Today we will prepare your computer for the course. We will install the basic tools, keep your API key safe, and run one small program that talks to an AI model.

You do not need AI or programming experience. I will explain every new word before we use it.

By the end, you will see a real AI answer in your terminal. You will also understand what your program sent, where it went, and why the request may cost a small amount of money.

Let us begin with the result we want.

[GO TO SLIDE 02.]

## 02. What ‘done’ looks like today.

[SLIDE 02 — Point to each card.]

This slide shows our finish line.

First, Python must work in the terminal. Python is the program that will run our course code.

Second, VS Code must open the course folder. This is where we will read and edit files.

Third, we need a virtual environment. This gives the course its own private set of Python packages.

Fourth, the API key must stay in a local file that Git will not upload.

Fifth, our first program must receive a real answer from an AI model.

Finally, you should understand what each part does. We do not want to copy commands without knowing why.

At the end of Day Zero, we will check all six results.

[GO TO SLIDE 03.]

## 03. Where Day 0 fits in the 40-day journey.

[SLIDE 03 — Move from left to right.]

Day Zero is the starting point for the full course.

In Phase One, we learn how language models, prompts, Python, and APIs work.

In Phase Two, we teach an AI system to find useful information in documents and answer with sources.

In Phase Three, we build safe agents that can use tools and ask for human approval.

In Phase Four, we connect larger workflows, MCP tools, and multiple agents.

In Phase Five, we test, secure, deploy, and monitor our systems.

In the final phase, we bring everything together in a production-style project.

The course is about more than building a demo. You will learn how to explain the system, test it, run it, and fix it when something goes wrong.

Today we build the foundation for all of that work.

[GO TO SLIDE 04.]

## 04. What is Agentic AI?

[SLIDE 04 — Follow the flow from left to right.]

Let us first understand Agentic AI in simple words.

Imagine a customer asks, “Where is my order?”

The AI model reads the question and decides what it needs. It may choose an approved tool that can look up the order.

The tool returns the order information. The system remembers that result. It then decides whether the job is complete or another step is needed.

This gives us four important parts.

The model thinks about the next step. Tools let the system do approved work. State remembers what has happened. The loop controls when to continue and when to stop.

A single AI answer is not a full agent. Today we start with that first small piece: one AI request and one answer.

[GO TO SLIDE 05.]

## 05. Model call, chatbot, workflow, or agent?

[SLIDE 05 — Walk down the table.]

We should not use an agent for every problem.

Use one model call when you need one simple result, such as a summary.

Use a chatbot when the main job is to have a conversation.

Use a normal workflow when the steps are already known. For example: check the input, change the data, and save it.

Use an agent when the next step depends on what the system finds. A support investigation is a good example because different problems may need different tools.

Agents can cost more, take longer, and create more safety questions. We should use one only when it gives us a real benefit.

Our first program is a simple model call. We will add more parts slowly in later lessons.

[GO TO SLIDE 06.]

## 06. The local toolkit — in plain language.

[SLIDE 06 — Point to each tool.]

These are the basic tools for the course.

Python runs our programs.

VS Code is the editor where we read and change our files. It also has a terminal built in.

Git keeps a history of our changes. This helps us see what changed and return to an older version if needed.

The AI provider account gives our program permission to use a model. That permission comes through an API key.

A virtual environment keeps this course’s Python packages separate from other projects.

The course repository is the main folder that contains the lessons, code, checks, and helper files.

We only install what we need now. We will add other tools later when the course reaches them.

[GO TO SLIDE 07.]

## 07. The terminal is where we prove things.

[SLIDE 07 — Point to the command and expected result.]

The terminal is where we run commands and check results.

Type python, then two hyphens, then version. Press Enter.

The terminal should show Python three point eleven or a newer version.

If Windows says Python is not recognized, it usually means Python was not added to PATH. PATH is simply the list of places where the computer looks for programs.

If you use a Mac and the python command does not work, try python three instead.

The important habit is this: do not stop after clicking Install. Run a command and check the result. The result is our proof that the installation works.

[GO TO SLIDE 08.]

## 08. Install Python and VS Code.

[SLIDE 08 — Begin the installation lab.]

Now let us install Python and VS Code.

Download Python from the official Python website. On Windows, select the option called Add python dot exe to PATH before you start the installation.

When the installation finishes, open a new terminal. A terminal that was already open may not see the new PATH setting.

Run the version command and check that the version is three point eleven or newer.

Next, install VS Code. Open VS Code, then open the complete course repository folder. Do not open only one file because we want the terminal to start in the correct project.

[LIVE DEMO — Install the tools, run the version check, and open the repository.]

Pause the video here. Continue only when the version command works and VS Code shows the course folder.

[GO TO SLIDE 09.]

## 09. Read the error before changing anything.

[SLIDE 09 — Show the error.]

Errors are normal. The important skill is learning how to read them.

This error says the terminal cannot find Python. It does not mean our AI code is wrong. The problem happens before our code can even run.

On Windows, the usual fix is to install Python again and select Add Python to PATH. Then close the old terminal, open a new one, and run the same version command.

Use this simple method whenever something fails.

First, read the first useful error line. Second, decide which part failed. Third, change only one thing. Fourth, run the same check again.

Changing many things at the same time makes the problem harder to understand.

[GO TO SLIDE 10.]

## 10. An API key is a credential.

[SLIDE 10 — Follow the request path.]

Before we use an AI service, we need to understand the API key.

An API key is like a password for a program. It tells the AI provider which account is making the request. That means a person who gets your key may be able to use your account and create charges.

Never put a real key inside your Python code. Do not show it in a video, screenshot, chat message, or Git commit.

Set a spending limit or alert in your provider account when that option is available.

If a key is ever shown by mistake, revoke it and create a new key. Simply hiding the text later is not enough because copies may already exist.

Also remember that your prompt is sent to the provider. For this first exercise, use simple test text and never use private business or customer data.

[GO TO SLIDE 11.]

## 11. Template in Git. Secret on your machine.

[SLIDE 11 — Point to the two file examples.]

We use two files for configuration, and they have different jobs.

Dot-env example is a safe template. It shows the names of the settings that the project needs. It contains fake values, so we can keep it in Git and share it.

Dot-env is the private local file. It contains your real API key. Git must ignore this file so it is not uploaded.

The dot-gitignore file lists files that Git should not track. In this project, it includes dot-env and other common secret file types.

Be careful: a file is not safe only because its name contains the word example. Never place a real key in dot-env example.

We will create the private file in the setup lab.

[GO TO SLIDE 12.]

## 12. Verify that Git ignores the secret.

[SLIDE 12 — Point to the command.]

We should check that Git really ignores the secret file.

From the main course folder, run git check-ignore dash v dot-env.

The output should show the ignore rule and the dot-env filename. The line number may be different on your computer, and that is fine.

If the command prints nothing, stop before making any Git commit. Check that the file is named exactly dot-env and that dot-gitignore contains the dot-env rule.

During a recording, do not open the real dot-env file. Use dot-env example when you need to explain the settings.

Security rules are stronger when we test them instead of only assuming they work.

[GO TO SLIDE 13.]

## 13. Create the project’s private toolbox.

[SLIDE 13 — Begin the project setup lab.]

Now we create a virtual environment for this course.

A virtual environment is a private Python toolbox for one project. Packages installed here will not mix with packages from other projects.

Run python dash m venv dot-venv.

On Windows PowerShell, run dot-venv backslash Scripts backslash Activate dot ps one.

On a Mac or Linux computer, run source dot-venv slash bin slash activate.

After activation, you should normally see dot-venv in parentheses at the start of the terminal line. That tells us the terminal is using this project’s Python environment.

[LIVE DEMO — Create and activate the environment. Point to the dot-venv name in the terminal.]

[GO TO SLIDE 14.]

## 14. Install pinned dependencies and the shared helper.

[SLIDE 14 — Keep the virtual environment active.]

Next, we install the Python packages used by the course.

The first command updates pip inside the virtual environment. Pip is the tool that installs Python packages.

The second command reads requirements dot txt and installs the package versions listed there.

The third command installs this course project in editable mode. This makes the shared AI helper available from every lab folder.

We use listed package versions so every learner starts with the same tested setup. Later, we can update versions carefully and test the changes.

[LIVE DEMO — Run the three commands. You do not need to read every installation line. Stop and explain any red error.]

[GO TO SLIDE 15.]

## 15. Create local configuration safely.

[SLIDE 15 — Do not show the real key.]

Now we create the private configuration file.

On Windows, copy dot-env example to dot-env. On a Mac or Linux computer, use the cp command shown on the slide.

Open dot-env and choose the provider you want to use. Paste the matching API key.

Do this while screen recording is stopped. A key can be captured by the video, terminal history, or automatic captions.

Close the file before you start recording again.

Then run the Git ignore check. Make sure Git reports that dot-env is ignored.

[LIVE DEMO — Copy the template. Stop recording. Add the key privately. Close the file, resume recording, and run the ignore check.]

[GO TO SLIDE 16.]

## 16. Run the setup gate.

[SLIDE 16 — Run the setup checker.]

Now we check the complete local setup.

Run the command shown on the slide from the main course folder.

The checker looks at your Python version, required packages, and the presence of the selected API key.

The output on this slide is only an example. Read the real result from your own terminal.

When everything is correct, the final line says All checks passed.

This checker does not contact the AI provider. It only checks that the key exists, so it does not prove that the key is valid and it does not use model tokens.

[LIVE DEMO — Run the checker. If one check fails, explain that line, fix one problem, and run the checker again.]

Do not continue until all checks pass.

[GO TO SLIDE 17.]

## 17. What happens during one AI request?

[SLIDE 17 — Follow the request from left to right.]

We are ready to make the first real AI request.

Our Python program creates a prompt. The course helper reads the provider settings from dot-env. The provider’s software sends the request over the internet. The model creates an answer, and the provider sends the answer back with usage information.

Three things are important.

First, the prompt leaves your computer. Do not send private information.

Second, the provider counts the text it reads and writes as tokens. This request may cost a small amount of money.

Third, the call depends on the internet and an outside service. A network problem, bad key, account limit, or provider problem can make the request fail even when our code is correct.

We will use a short and harmless prompt.

[GO TO SLIDE 18.]

## 18. The smallest useful program.

[SLIDE 18 — Explain the code one line at a time.]

This is our first small AI program.

The first line imports the ask helper from the course.

The second part creates a prompt. A prompt is the instruction or question we send to the model.

The ask function sends that prompt using the provider settings from dot-env.

The print function shows the result in the terminal.

The helper makes this first lesson shorter by handling provider setup for us. The request still goes over the internet and still uses the API key.

Later lessons will show more details, including structured results, retries, errors, tools, tests, and traces.

[LIVE DEMO — Open the starter file and complete the missing lines. Explain each line while you type it.]

[GO TO SLIDE 19.]

## 19. Run the first real AI call.

[SLIDE 19 — Run the program.]

Now run the Hello AI program with the command on the slide.

This is the first step today that contacts the AI provider. It may create a small charge.

Your answer will probably not use the exact words shown here. AI-generated text can change from one run to another.

We are looking for two things: a useful answer and a usage line that tells us which provider and model were used and how many tokens were counted.

[LIVE DEMO — Run the command. Read the real answer and the real usage information.]

One successful call proves that this path works now: this computer, this setup, this network, and this provider account.

It does not prove that every future call will work or that the system is ready for production.

[GO TO SLIDE 20.]

## 20. Change one variable and observe.

[SLIDE 20 — Ask the learner to predict first.]

Let us change the prompt and see what happens.

Ask the model to explain an API key to a ten-year-old in two sentences.

Before running the program, make a prediction. The answer should use simple words, talk about API keys, and stay close to two sentences.

[LIVE DEMO — Change only the prompt, save the file, and run the program again.]

Now compare the result with the prediction.

Did the answer use simple language? Did it follow the two-sentence request? Did the token count change?

This is a basic experiment: change one thing, predict the result, run it, and compare the evidence.

One good answer is not enough to prove that a prompt is always reliable. We will learn proper testing later in the course.

[GO TO SLIDE 21.]

## 21. Find the failing layer.

[SLIDE 21 — Walk down the table.]

If the first call fails, use the message to find the part that failed.

If Python is not recognized, check the Python installation and PATH.

If Python says there is no module named shared, make sure the virtual environment is active and that you ran pip install dash e dot.

If the key is missing, check dot-env, the selected provider, and the matching key name.

If you receive a four-oh-one error, the provider rejected the login details. Check the key, account, and extra spaces.

A four-two-nine error usually points to a request limit, provider capacity, or account limit.

A timeout may be caused by your internet connection, a company proxy, or the provider.

Always read the real error. Never share a secret when asking for help.

[GO TO SLIDE 22.]

## 22. Know what you send and what you spend.

[SLIDE 22 — Point to Before, After, and Account.]

Every AI request uses data and resources.

Before a call, ask: is this prompt safe to send? Which provider and model will receive it?

After the call, look at the usage. Ask whether the result was useful enough to justify the request.

In the provider account, use spending limits, alerts, and access controls when they are available.

The simple cost idea is: input tokens multiplied by the input price, plus output tokens multiplied by the output price.

Providers may price some token types differently. Prices and model names can also change.

That is why we do not promise an exact cost in this lesson. Check the current provider pricing and your real account usage.

[GO TO SLIDE 23.]

## 23. Build → break → prove → record.

[SLIDE 23 — Follow the four-step loop.]

This course uses a simple working habit: build, break, prove, and record.

First, build the smallest working version.

Second, create one safe and controlled failure so you understand what can go wrong.

Third, prove both results with a command, test, or other clear evidence.

Fourth, record what worked and what is still limited.

For Day Zero, the working path is the first AI reply. A safe failure might be a missing package or missing key.

Later projects will add tests, evaluation data, logs, approval steps, deployment checks, rollback plans, and incident practice.

The main idea is simple: code existing on a computer is not proof that the system works. We need evidence.

[GO TO SLIDE 24.]

## 24. Can you explain the setup boundary?

[SLIDE 24 — Keep the answers closed at first.]

Let us check what we learned.

Why do we use a virtual environment?

[WAIT, THEN OPEN QUESTION 1.]

It keeps this project’s packages separate and makes the setup easier to repeat.

Why do we share dot-env example but not dot-env?

[WAIT, THEN OPEN QUESTION 2.]

The example contains safe placeholders. Dot-env contains the real secret.

Does the setup checker prove that the API key is valid?

[WAIT, THEN OPEN QUESTION 3.]

No. It checks that the key exists. The real model call tests whether the provider accepts it.

What information crosses the internet during the first call?

[WAIT, THEN OPEN QUESTION 4.]

The prompt and request details go to the provider. The answer and usage information come back.

[GO TO SLIDE 25.]

## 25. Day 0 readiness check.

[SLIDE 25 — Check each item using real evidence.]

This is the final Day Zero checklist.

Mark an item only after you have checked it on your own computer.

Confirm that Python works in a new terminal and VS Code opens the repository.

Confirm that dot-venv is active and the packages are installed.

Confirm that dot-env contains the selected provider key and Git ignores the file.

Confirm that the setup checker passes and the first AI call returns an answer with usage information.

Confirm that no secret appears in your code, Git history, screenshots, or terminal history.

Finally, make sure you can explain what data was sent and why the request may cost money.

If one item is not complete, stop and fix it before Day One.

[GO TO SLIDE 26 WHEN ALL ITEMS ARE COMPLETE.]

## 26. Your machine can now makea controlled AI request.

[SLIDE 26 — Close the main lesson.]

Your computer is now ready for the next lesson.

Python and VS Code work. The project has its own virtual environment and packages. Your API key stays in a local file that Git ignores. The setup checker passes, and your program has received a real AI answer.

You also understand the important boundaries. The prompt leaves your computer. The API key gives access to your account. The model call can cost money. The internet or provider can fail.

In Day One, we will look more closely at language models, tokens, context, and prompts. We will turn today’s first call into a repeatable program that we understand clearly.

Keep this setup. Every later lab builds on it.

[END THE MAIN LESSON OR GO TO THE REFERENCE SLIDE.]

## 27. Day 0 recording companion.

[SLIDE 27 — Optional reference slide.]

This Day Zero folder contains the presentation, the full speaking transcript, the recording guide, and a PDF copy of the slides.

The lesson follows the production-ready course outline and the existing Day Zero labs.

The terminal results shown in the slides are examples. During a real demonstration, always explain what your own terminal actually shows.

Before publishing the video, check current provider model names, prices, account rules, and installation steps because these details can change.

[END.]
