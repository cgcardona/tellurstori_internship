# Intern Onramp Roadmaps: Web Tech & Unix Terminal

Audience: Sol, Harper, Toby, Ben  
Expected Level: Smart beginners, no prior programming required  
Pace: Self‑guided, evenings/weekends, with weekly pair‑programming check‑ins

---

## How to Use This Document

This document is written so you can:
- Read it **alone** without a teacher present
- Try things immediately on your own computer
- Re‑read sections as many times as needed

If something doesn’t click at first, that’s normal. Understanding comes from *doing*, not memorizing.

Whenever you see:
- **▶ Try This** — you should actually do it
- **⚠ Common Mistake** — slow down and read carefully

---

# Roadmap A — Web Technology Fundamentals

## Phase 0 — Mental Models: How the Web Actually Works

### What Is the Web?

At its core, the web is a **conversation between computers**.

One computer asks for something. Another computer responds.

That’s it.

Everything else — websites, apps, videos, social media — is built on top of that simple idea.

---

### Clients and Servers

- A **client** is a device or program that *requests* data
  - Examples: your browser, a phone app, a SwiftUI app
- A **server** is a computer that *responds* to requests
  - Servers are usually always on and connected to the internet

Clients:
- initiate communication
- ask questions

Servers:
- wait for requests
- return answers

---

### What Happens When You Type a URL?

Example:
```
https://example.com
```

Step by step:
1. Your browser asks the internet: “Where is example.com?” (DNS)
2. It opens a secure connection to that server (HTTPS)
3. It sends an **HTTP request** saying:
   > “Please send me the homepage”
4. The server responds with:
   - HTML
   - images
   - other resources
5. Your browser reads the HTML and builds the page

---

### ▶ Try This: Inspect a Real Website

1. Open any website
2. Right‑click → Inspect
3. Click the **Network** tab
4. Refresh the page

You will see:
- HTML documents
- images
- API requests

Every modern app does this.

---

### Why Native Apps Still Use Web Tech

Even though TellUrStori is written in SwiftUI:
- it still sends HTTP requests
- it still receives JSON
- it still talks to servers

If you understand the web, you understand how *apps talk to the world*.

---

## Phase 1 — HTML & the DOM

### What HTML Actually Is

HTML stands for **HyperText Markup Language**.

HTML:
- does NOT control logic
- does NOT control styling
- DOES describe **structure and meaning**

Think of HTML as the *skeleton* of a page.

---

### Basic HTML Example

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

Important ideas:
- Tags open and close
- Indentation shows hierarchy

---

### Nesting and Structure

HTML forms a **tree**:

```html
<article>
  <h2>Title</h2>
  <p>Text</p>
</article>
```

`article` is the parent  
`h2` and `p` are children

⚠ Closing tags incorrectly breaks the tree.

---

### Semantic HTML

Semantic tags describe *meaning*:
- `<header>`
- `<nav>`
- `<main>`
- `<article>`
- `<footer>`

Why this matters:
- Accessibility
- Search engines
- Maintainability

---

### The DOM (Document Object Model)

When the browser loads HTML:
- it converts it into a **live object tree** called the DOM
- every element becomes a node

The DOM is what:
- JavaScript manipulates
- automation tools inspect
- UI systems mirror

Understanding the DOM = understanding UI frameworks.

---

### ▶ Try This: Live DOM Editing

1. Inspect a webpage
2. Find an `<h1>`
3. Double‑click the text
4. Change it

You just modified the DOM in real time.

---

## Phase 2 — HTTP & APIs

### What Is HTTP?

HTTP = **HyperText Transfer Protocol**

It defines:
- how requests are sent
- how responses are formatted

HTTP is:
- stateless
- predictable
- universal

---

### HTTP Methods (Verbs)

| Method | Meaning |
|------|--------|
| GET | Fetch data |
| POST | Create new data |
| PUT | Update existing data |
| DELETE | Remove data |

---

### Status Codes

Servers respond with status codes:

| Code | Meaning |
|----|--------|
| 200 | Success |
| 400 | Bad request |
| 401 | Unauthorized |
| 404 | Not found |
| 500 | Server error |

Machines use these instead of words.

---

### JSON

JSON = **JavaScript Object Notation**

Example:
```json
{
  "id": 42,
  "name": "Sol",
  "active": true
}
```

Why JSON?
- Human readable
- Language independent
- Maps cleanly to data structures

---

### ▶ Try This: curl

```bash
curl https://api.github.com
```

You just made an HTTP GET request.

---

## Phase 3 — From Web to App Thinking

### APIs as Contracts

An API is a promise:
- If you send this request
- You will receive this response

Breaking that promise breaks apps.

---

### JSON → Swift Example

```swift
struct User: Codable {
  let id: Int
  let name: String
}
```

Keys must match JSON fields.

---

### ▶ Try This

Take JSON from a real API and model it in Swift.

---

# Roadmap B — Unix Terminal & Workflow

## Phase 0 — Terminal Orientation

### What Is the Terminal?

The terminal is a text interface to your computer.

It gives:
- more control
- more power
- more responsibility

---

### Filesystem Basics

Everything lives in a tree:

```
/
├── Users
│   └── you
│       └── Projects
```

---

### ▶ Try This

```bash
pwd
ls
cd ~
```

---

## Phase 1 — Core Commands

Commands:
- `ls` — list
- `cd` — change directory
- `mkdir` — make directory
- `rm` — remove

⚠ `rm -rf` deletes permanently.

---

## Phase 2 — Pipes & Processes

Unix philosophy:
> Small tools combined do powerful things.

Example:
```bash
ls | grep txt
```

---

## Phase 3 — Git

Git tracks history.

Basic flow:
```bash
git clone
git add
git commit
git push
```

---

## Phase 4 — AI‑Augmented Workflow

AI helps you:
- move faster
- explore ideas

AI does NOT replace understanding.

Always ask:
- Does this make sense?
- Can I explain it?

---

## Graduation Criteria

You graduate when you can:
- Explain HTTP end‑to‑end
- Read HTML confidently
- Use the terminal safely
- Collaborate using Git
- Use AI responsibly

This document is meant to be *used*, not just read.
Break things. Fix them. Learn.

