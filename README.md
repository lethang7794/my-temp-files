# my-temp-files

A collections of temporary files to be used with code editor (and have syntax highlighting)

## Motivation

1. I need a place to quickly save temporary code snippet and notes (in Markdown)

2. I need to be able to to close "whatever I'm using" without worrying of losing what I just save.

3. It needs to show code with syntax highlight.

4. It needs to be blazing fast, so it doesn't disrupt my flow of thinking.

5. It needs to work with my daily IDE (VS Code) and other IDE/text editor (Goland, Sublime Text).

## Prerequisite

- git

## How to start

1. Clone this repo

   ```bash
   git clone git@github.com/lethang7794/my-temp-files
   ```

   or

   ```bash
   git clone https://github.com/lethang7794/my-temp-files.git
   ```

2. Ignore it for all repos

   - Config git global ignore file, e.g. `~/.gitignore`

     ```bash
     git config --global core.excludesfile ~/.gitignore
     touch ~/.gitignore
     ```

   - Add to `.gitignore` file

     ```txt
     .my-temp-files
     ```

3. Make a symlink to your $HOME directory

   ```bash
   ln -s PATH_TO_THIS_REPO ~/.my-temp-files
   ```

4. (In your working repository), make a symlink to the symlink you've just made

   ```bash
   # In your working repository
   ln -s  ~/.my-temp-files ./.my-temp-files
   ```

## How to use

### Option 1: Open file directly with your IDE/text editor

e.g

- Use nano

  ```bash
  nano ~/.my-temp-files/markdown.md
  ```

- Use Sublime Text

  ```bash
  subl ~/.my-temp-files/markdown.md
  ```

### Option 2: Quickly open file in IDE/text editor (needs to make a symlink in your working repo)

e.g.

- For VS Code, use `Go to File...` (`Ctrl + P`)

- For Goland, use
  - `Go to File` (`Ctrl + P`)
  - `Search Everywhere` (`Ctrl + Shift + A` or `F1`)
