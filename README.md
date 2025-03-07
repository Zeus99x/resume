# Hosting Your Resume with Markdown and GitHub Pages

## Purpose

This README explains how to create and host your resume as a static website using tools recommended by Andrew Etter in _Modern Technical Writing_, such as Markdown and Git. It guides you through the steps to build your own site, connecting each step to Etter’s ideas about efficient documentation. Whether you’re following along or just exploring, this is written for individuals familiar with Markdown but new to Git, static site generators, and forges, with a basic understanding of their computer’s command line.

## Prerequisites

Before you start, you’ll need a few tools. Don’t worry—the setup is straightforward, and the instructions assume a Windows system (though they can be adapted for other operating systems).

1. **Git**: A version control system to manage your files. Download it from [git-scm.com](https://git-scm.com/).
2. **Python**: Required for the Pelican static site generator. Get it at [python.org](https://python.org/).
3. **Pelican**: A tool that converts Markdown into a website. Install it later with a command provided below.
4. **GitHub Account**: A free account on [github.com](https://github.com/) to host your work.
5. **Markdown Editor**: Use Notepad for simplicity, or try Visual Studio Code (from [code.visualstudio.com](https://code.visualstudio.com/)) for a live preview of your Markdown.

You’ll also need your resume content ready—feel free to use your own or create a sample. Basic command-line skills (like `cd` to change directories) will help, but the steps are kept simple.

## Instructions

Here’s how to build and host your resume. Each step follows guidelines from William S. Pfeiffer’s _Technical Communication_—using one action per step and starting with a verb—to ensure clarity. The steps also tie into Etter’s principles from _Modern Technical Writing_.

### 1. Install Git

- **Action**: Download Git from [git-scm.com](https://git-scm.com/) and run the installer. Accept the defaults by clicking “Next” until installation completes.
- **Etter’s Principle**: Etter values distributed version control systems like Git for tracking changes and enabling collaboration, keeping your work safe and organized.

### 2. Set Up Git on Your Computer

- **Action**: Open the Command Prompt (search “cmd” in Windows), then type `git config --global user.name "Your Name"` and press Enter. Next, type `git config --global user.email "your.email@example.com"`.
- **Etter’s Principle**: Etter emphasizes that tools should be simple to start with. These commands configure Git with your identity, preparing it for your project.

### 3. Create a GitHub Repository

- **Action**: Go to [github.com](https://github.com/), sign in (or sign up), and click “New Repository.” Name it “resume,” make it public, and click “Create Repository.”
- **Etter’s Principle**: Etter recommends forges like GitHub for sharing documentation, providing an online storage space.

### 4. Clone the Repository to Your Computer

- **Action**: On your repository page, click the green “Code” button, copy the URL (e.g., `https://github.com/yourusername/resume.git`), then in Command Prompt, type `git clone [paste URL]` and press Enter.
- **Etter’s Principle**: Distributed systems allow local work with online synchronization, copying your GitHub folder to your PC.

### 5. Write Your Resume in Markdown

- **Action**: Open a text editor (e.g., Notepad), write your resume (e.g., `# Your Name\n## Experience\n- **Job Title, Company**`), and save it as `resume.md` in the cloned repository folder.
- **Etter’s Principle**: Etter praises lightweight markup like Markdown for its speed and readability, ideal for content-focused writing.

### 6. Install Pelican

- **Action**: Open Command Prompt, type `pip install pelican markdown`, and press Enter. Wait for the installation to complete.
- **Etter’s Principle**: Static site generators like Pelican turn simple Markdown into websites, promoting efficiency as Etter suggests.

### 7. Set Up a Pelican Project

- **Action**: In Command Prompt, navigate to your repository folder with `cd resume`, then type `pelican-quickstart`. Answer the prompts: say “yes” to a content folder, “no” to articles, and accept defaults otherwise.
- **Etter’s Principle**: Etter values tools that automate formatting, and Pelican sets up your site structure efficiently.

### 8. Add Your Resume to the Content Folder

- **Action**: Move `resume.md` into the “content” folder inside the repository using File Explorer.
- **Etter’s Principle**: Keeping source files separate (e.g., in “content”) aligns with Etter’s organized workflow ideas.

### 9. Generate the Website

- **Action**: In Command Prompt, while in the repository folder, type `pelican content` and press Enter. This creates an “output” folder with your site.
- **Etter’s Principle**: Static sites are lightweight and fast to deploy, aligning with Etter’s preference over heavy dynamic systems.

### 10. Push Your Site to GitHub

- **Action**: Type `git add .`, then `git commit -m "Add my resume site"`, followed by `git push`. This uploads everything to GitHub.
- **Etter’s Principle**: Sharing via a forge like GitHub makes your work accessible, a key goal for Etter.

### 11. Enable GitHub Pages

- **Action**: On GitHub, go to your repository’s “Settings,” scroll to “Pages,” set the branch to “gh-pages” and folder to “/ (root),” then click “Save.” Wait a minute, then visit the link provided (e.g., `https://yourusername.github.io/resume`).
- **Etter’s Principle**: Hosting statically on a forge is simple and reliable, fitting Etter’s ideal for technical documentation.

These steps should get your resume online! If something’s unclear, feel free to review the resources below or seek further assistance.

## Further Resources

Here are some helpful links:

- [Markdown Guide](https://www.markdownguide.org/) – A great tutorial to polish your Markdown skills.
- [Git Basics](https://git-scm.com/docs/gittutorial) – Learn more about Git commands.
- [Pelican Documentation](https://docs.getpelican.com/) – Details on tweaking your site.
- [GitHub Pages Guide](https://pages.github.com/) – Official help for hosting your site.

## FAQ

### Why is Markdown better than writing raw HTML?

Markdown is simpler and quicker to write. Etter describes it as a lightweight way to focus on content rather than code.

### I updated my resume.md, but the website didn’t change. Why?

You need to regenerate the site and push it again. Run `pelican content`, then `git add .`, `git commit -m "Update resume"`, and `git push`. GitHub Pages only displays what’s uploaded to the repository.

### How do I update my resume on the website?

To update your resume, simply edit the `resume.md` file in your repository, regenerate the site using `pelican content`, and push the changes to GitHub. Your updates will then be reflected on your live website.

### How can I customize the theme of my resume website?

Pelican supports various themes to customize the look of your website. You can choose a theme from the [Pelican themes site](https://github.com/getpelican/pelican-themes) or create your own. After choosing a theme, you can modify the settings in the `pelicanconf.py` file to apply it to your site.

### Credits

- **Saman HM** - Author
- **Duc Can Thai** - Peer reviewer
- **Mehedi** - Peer reviewer
