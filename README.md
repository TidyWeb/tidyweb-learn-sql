# Learn SQL

This is a browser-based practice course for learning SQL from first queries through joins, summaries, subqueries, and controlled table changes. It also includes a small Python-to-SQL bridge.

This is Book 2 of the learning route. Start with [Book 1, Learn Python Data Preparation](https://tidyweb.github.io/tidyweb-learn-python-data-preparation/) if you first need to learn how to prepare a clean table for SQL.

You can [use the published SQL course online](https://tidyweb.github.io/tidyweb-learn-sql/) without installing anything. The instructions below are for anyone who wants their own complete copy on their computer.

## Getting the course onto your computer

This guide assumes you have never downloaded a GitHub project, used Git, opened a terminal in a folder, or started a local web server.

You do not need to understand every command yet. Follow one step at a time, in order, and do not skip the checks.

### What you are going to do

You will:

1. create an empty folder for the course;
2. download the complete course using Git or a ZIP file;
3. open a terminal in the correct folder;
4. start a small local web server; and
5. open the course in your browser.

Keep the whole course together. Do not move individual HTML files or the `datasets`, `guide`, `exercises`, or `shared` folders elsewhere.

### Before you begin

You need:

- an internet connection;
- a web browser; and
- Python 3 installed on your computer.

If you choose the Git method, you also need Git installed. The instructions include a check. If Git is not installed, you can use the ZIP method instead.

Commands are shown in boxes like this:

```bash
example command
```

Type or paste only the command. Do not type the word `bash`, the three backticks, or other text around the command.

---

## Step 1 — Choose Git or ZIP

There are two ways to put the course on your computer. Choose one; you do not need to do both.

### Git method

Choose Git if you want to practise Git and GitHub. Git can also make future course updates easier.

### ZIP method

Choose ZIP if you do not have Git or want the simplest download. You receive the same course files, but your folder will not be connected to GitHub.

---

## Step 2 — Create one empty course folder

Choose where the course will live. Your Documents folder is a sensible place.

1. Open your computer's file manager:
   - **Fedora/KDE:** open **Dolphin**.
   - **macOS:** open **Finder**.
   - **Windows:** open **File Explorer**.
2. Open **Documents**, or another place you can find again.
3. Create a new folder named `Learn SQL`.
4. Open the new folder.

The folder must be empty before you continue. Do not use the general Downloads folder as the course folder.

---

## Step 3A — Git method: open a terminal before cloning

If you chose ZIP, skip to **Step 3B**.

A terminal is a window where you give the computer written commands. You must open it inside the empty `Learn SQL` folder you just created.

### Fedora/KDE Plasma

1. Open the empty `Learn SQL` folder in Dolphin.
2. Right-click an empty part of the folder window. Do not right-click a file.
3. Choose **Open Terminal Here**.

If that choice is not shown, press **F4** in Dolphin. A terminal panel opens at the bottom of the folder window.

### macOS

Use either method below.

**Finder menu**

1. Find the `Learn SQL` folder in Finder.
2. Right-click the folder.
3. Choose **Services → New Terminal at Folder** if that choice is available.

**Drag the folder into Terminal**

1. Open the **Terminal** application.
2. Type `cd` followed by one space. Do not press Enter yet.
3. Drag the `Learn SQL` folder from Finder into the Terminal window.
4. Press **Enter**.

### Windows

Use either method below.

**Right-click inside the folder**

1. Open the empty `Learn SQL` folder in File Explorer.
2. Right-click an empty part of the folder window.
3. Choose **Open in Terminal**.

**Use the address bar**

1. Open the empty `Learn SQL` folder in File Explorer.
2. Click the address bar at the top of the window.
3. Type `powershell`.
4. Press **Enter**.

### Check that the terminal is in the empty folder

On Fedora or macOS, run these commands one at a time:

```bash
pwd
ls -la
```

On Windows PowerShell, run:

```powershell
Get-Location
dir -Force
```

The location shown should end with `Learn SQL`. The file list should not contain another project.

If the location is wrong, close the terminal and repeat the instructions above. Do not clone the course until the location is correct.

### Check that Git is installed

Run:

```bash
git --version
```

If you see a Git version number, continue. If you see `command not found`, `git is not recognized`, or a similar message, install Git and repeat the check, or use the ZIP method.

### Clone the course

Copy the complete command below, paste it into the terminal, and press **Enter**:

```bash
git clone https://github.com/TidyWeb/tidyweb-learn-sql.git .
```

The dot at the very end is part of the command. It means: put the course inside the folder I am already in.

Wait until the normal terminal prompt returns. If Git says the destination is not empty, stop. Do not force it or delete unknown files. Start again with a new empty folder.

Now continue to **Step 4**.

---

## Step 3B — ZIP method: download and extract the course

If you completed the Git method, skip to **Step 4**.

### Download the ZIP from GitHub

1. Open the [Learn SQL repository on GitHub](https://github.com/TidyWeb/tidyweb-learn-sql).
2. Click the green **Code** button near the top of the page.
3. Click **Download ZIP**.
4. Wait for the download to finish.

The downloaded file will usually be in your Downloads folder and its name will end in `.zip`.

### Move and extract the ZIP

1. Move the downloaded ZIP into the empty `Learn SQL` folder you created in Step 2.
2. Extract it:
   - **Fedora/KDE:** right-click the ZIP and choose **Extract → Extract Archive Here**.
   - **macOS:** double-click the ZIP.
   - **Windows:** right-click the ZIP, choose **Extract All**, check the destination, then click **Extract**.
3. Open the extracted folder. Keep opening folders until you see all of these items together:

```text
index.html
datasets
exercises
guide
shared
```

This is the course folder. From now on, “course folder” means this exact folder, not the ZIP and not the folder above it.

### Open a terminal in the extracted course folder

- **Fedora/KDE:** right-click an empty area and choose **Open Terminal Here**. If needed, press **F4** in Dolphin.
- **macOS:** right-click the folder and choose **Services → New Terminal at Folder**. If that is unavailable, use the drag-the-folder method from Step 3A.
- **Windows:** right-click an empty area and choose **Open in Terminal**, or click the File Explorer address bar, type `powershell`, and press **Enter**.

The folder is no longer empty because it contains the course. That is correct for the ZIP method.

---

## Step 4 — Prove you are in the correct course folder

Do this check whether you used Git or ZIP.

On Fedora or macOS, run:

```bash
pwd
ls
```

On Windows PowerShell, run:

```powershell
Get-Location
dir
```

The list must include:

```text
index.html
datasets
exercises
guide
shared
```

If you cannot see `index.html`, stop. You are in the wrong folder. Find the folder containing the items above, then open a new terminal there.

---

## Step 5 — Check that Python is installed

The course itself runs in your browser. Python is used here only to start a small local web server so every part of the course loads correctly.

### Fedora or macOS

Run:

```bash
python3 --version
```

### Windows PowerShell

Run:

```powershell
py --version
```

If you see a Python 3 version number, continue. If the command is not found, install Python 3, reopen the terminal in the course folder, and repeat the check.

---

## Step 6 — Start the course

Keep the terminal open in the course folder.

### Fedora or macOS

Run:

```bash
python3 -m http.server 8000
```

### Windows PowerShell

Run:

```powershell
py -m http.server 8000
```

The terminal should show a message that it is serving files on port 8000. Leave this terminal running.

Open your web browser and go to:

<http://localhost:8000/>

You should see the Learn SQL home page. Choose **Learner's Guide** to begin.

The course's browser-based Python and SQL tools are loaded from the internet, so keep your internet connection active while using the interactive exercises.

---

## Step 7 — Stop the course safely

Return to the terminal that is running the server. Hold **Ctrl** and press **C** once.

The server stops and the normal terminal prompt returns. You can now close the browser tab and terminal. The course files remain on your computer.

---

## What to do every later study session

Do not download the course again.

1. Open your existing `Learn SQL` course folder.
2. Open a terminal in the folder containing `index.html`.
3. Start the local server again:
   - **Fedora or macOS:** `python3 -m http.server 8000`
   - **Windows:** `py -m http.server 8000`
4. Open <http://localhost:8000/> in your browser.
5. Press **Ctrl+C** in the terminal when you finish.

---

## Common problems

### I do not know which folder the terminal is using

Run `pwd` on Fedora or macOS. Run `Get-Location` in Windows PowerShell. Compare the result with the course folder shown in your file manager.

### I cannot see `index.html`

You are not in the course folder. The ZIP method often creates an extra folder level. Find the folder containing `index.html`, `datasets`, `exercises`, `guide`, and `shared`, then open a new terminal there.

### `git` is not recognized or `git: command not found`

Git is not installed or the terminal has not noticed a new installation. Install Git and reopen the terminal, or use the ZIP method.

### Git says the destination is not empty

Do not clone over existing files. Create a different empty folder, open a terminal there, check its location, and run the clone command again.

### Python is not recognized or not found

Install Python 3, then reopen the terminal in the course folder. On Fedora or macOS, use `python3`. On Windows, use `py`.

### The browser says it cannot reach the page

Check that the server command is still running in the terminal. If you closed the terminal or pressed **Ctrl+C**, start the server again.

### Port 8000 is already in use

Another local server may already be using that port. Start this course on port 8001 instead:

- **Fedora or macOS:** `python3 -m http.server 8001`
- **Windows:** `py -m http.server 8001`

Then open <http://localhost:8001/>.

### A practice page opens but an interactive tool does not load

Keep your internet connection active. Refresh the page after the connection returns. Also check that you opened the course through `http://localhost:8000/`, not by double-clicking an individual HTML file.

---

## Suggested learning route

1. Open the **Learner's Guide** from the course home page.
2. Read the overview before attempting a practice lab.
3. Work through Chapters 1 to 6 in order.
4. Use the practice labs to repeat each group of ideas.
5. Use the reference pages when a piece of syntax needs a reminder.
6. Try the Coffee Python SQL Bridge after the SQL foundations are familiar.

You can also [open the learner's guide directly](guide/html/SQLBolt%20Compressed%20Map.html).

## What is included

- `guide/` — the learner's guide, chapters, references, and logo
- `exercises/` — interactive SQL practice labs and the Python-to-SQL bridge
- `datasets/` — CSV files used by the exercises
- `shared/` — navigation used by the learner pages
- `* Lab Cheat Sheet.html` — optional answer references for the practice labs
