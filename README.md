🐧 OverTheWire Bandit
question everything. understand anything.

<p align="center">
<img src="https://img.shields.io/badge/FOCUS-LINUX-8B9D83?style=flat-square" alt="Focus: Linux" />
<img src="https://img.shields.io/badge/NETWORKING-SSH-8B9D83?style=flat-square" alt="Networking and SSH" />
<img src="https://img.shields.io/badge/LEVEL-BEGINNER-C9A66B?style=flat-square" alt="Beginner level" />
<img src="https://img.shields.io/badge/STATUS-LEARNING-7D8590?style=flat-square" alt="Learning in progress" />
</p>

<p align="center">
<i>A journey through Linux, networking, and cybersecurity — one question at a time.</i>
</p>

00 — The idea

Most people want to know which command works.

I want to know why it works.

Why does a file named - behave differently?
Why does SSH need a port?
What actually happens when two computers communicate?
Why does one command work while another fails?

This repository is my attempt to find the answers.

I'm documenting my journey through the OverTheWire Bandit wargame, exploring Linux, networking, SSH, and the fundamentals of cybersecurity along the way.

Not just solutions. Not just commands to copy and paste.

Experiments, mistakes, observations, and the reasoning behind them.

The goal isn't to memorize the answer. It's to develop the ability to find your own.
01 — What's inside?
Area	Exploring
01 / Linux	Filesystems, permissions, paths, shell commands
02 / Networking	IP addresses, ports, DNS, TCP, client-server communication
03 / SSH	Remote access, authentication, encrypted connections
04 / Investigation	File types, hidden files, text searching, unusual filenames
05 / Cybersecurity	CTF challenges, troubleshooting, analytical thinking
06 / The CLI	Pipes, redirection, arguments, standard input and output

Each topic is another piece of the bigger picture.

02 — A little terminal magic
Connecting to a remote machine
bash
ssh bandit0@bandit.labs.overthewire.org -p 2220


A single command, multiple concepts.

ssh → the client used to establish a secure remote session
bandit0 → the username
bandit.labs.overthewire.org → the remote hostname
-p 2220 → the port used by the SSH service

Instead of treating this as a command to memorize, I want to understand what each part contributes to the connection.

When a filename looks like an option

Imagine a file literally named -.

bash
file ./-
cat ./-


Why ./- instead of simply -?

Because command-line programs can interpret arguments beginning with a dash as options. Prefixing the filename with ./ makes it an explicit path relative to the current directory.

Another approach is:

bash
cat -- -


Here, -- marks the end of options for cat.

A tiny detail. A useful lesson.

The interesting part isn't just getting the output. It's understanding the behavior that produced it.

03 — The learning process

My approach is simple:

text
OBSERVE  →  QUESTION  →  EXPERIMENT  →  UNDERSTAND  →  DOCUMENT


01. Observe

Look at the environment and the information available.

02. Question

What seems unusual? What am I assuming? What don't I understand yet?

03. Experiment

Try an approach, read the output, and investigate unexpected results.

04. Understand

Work out why it happened instead of settling for a working command.

05. Document

Write down the discovery so the lesson remains useful beyond that one challenge.

There isn't always one correct path. Exploring alternatives is part of the process.

04 — Repository map
text
overthewire-bandit-walkthrough/
│
├── README.md
│
├── bandit_0.txt
├── bandit_1.txt
├── bandit_2.txt
├── bandit_3.txt
│
└── ...


The level notes remain in plain-text format.

Each file captures part of the journey: the problem, the commands, the observations, and the questions that helped me understand what was happening.

The structure may evolve as the collection grows. The purpose stays the same.

05 — Useful rabbit holes
Resource	Why it's here
OverTheWire Bandit	The challenges that started this journey
OpenSSH Manual	Understanding SSH beyond its syntax
GNU Coreutils	Exploring everyday command-line tools
MDN — HTTP Overview	Understanding web communication
Cloudflare Learning Center	Exploring networking and security fundamentals

Read the documentation. Test what you learn. Follow the questions wherever they lead.

06 — Who is this for?

For the curious ones.

For beginners learning Linux. For people exploring networking and cybersecurity. For anyone who has ever run a command, seen the output, and wondered:

Wait. Why did that happen?

You don't need to know everything before you start.

You just need to keep asking better questions.

<p align="center">
<b>THE TERMINAL IS THE PLAYGROUND.</b>
<br/>
<code> curiosity > memorization </code>
<br/><br/>
<i>Learn the command. Understand the system. Find your own way.</i>
</p>

<p align="center">
<sub>Educational purposes only · Authorized security practice</sub>
</p>
