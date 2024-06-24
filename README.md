## Title: **Guide to Basic Edits of the Webpage**

------------------------------------------------------------------------

### Introduction

-   **Purpose**: The purpose of this guide is to provide users with clear, step-by-step instructions on how to perform basic edits and customization tasks on a Quarto website. Whether you're looking to modify content, update styles, or restructure the site, this guide will help you understand which files to edit and how to publish your changes effectively using GitHub Desktop and RStudio. This ensures that your website remains up-to-date, well-maintained, and aligned with your specific needs and goals.

------------------------------------------------------------------------

### Table of Contents

1.  Accessing the Quarto Project
2.  Understanding the Project Structure
3.  Editing Content
4.  Previewing Changes
5.  Publishing Updates
6.  Troubleshooting Tips
7.  Additional Resources

------------------------------------------------------------------------

### 1. Accessing the Quarto Project

-   **Step 1**: Make sure the rmarkdown package is installed in R-studio. Open R-studio, click the packages tab in the lower left hand corner, click install packages, type in rmarkdown, make sure "install dependencies" is clicked on, then press install. Close R-studio.

-   **Step 2**: Install Quarto. This webpage is built using Quarto, an open-source scientific and technical publishing system that enables you to create and share documents, presentations, and websites with a focus on reproducibility.
    -   Follow the instruction to install Quarto here: https://quarto.org/docs/get-started/.

-   **Step 3**: Install GitHub Desktop from: https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop
    
-   **Step 3**: Clone the repository
    -   Instructions on how to clone the repository from GitHub can be found in the following link:
        https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-and-forking-repositories-from-github-desktop

-   **Step 4**: Open project in R-Studio: Inside R-studio you should see a files tab in the bottom right hand corner. Most files you click will be opened up as text files in the R-studio editor. Click the "Index.Rmd" file.

-   **Step 5**: To compile the entire website, find the build tab in the top right hand corner. You should see the option to "build website". Click this. The website should be built.

-   **Step 4**: After the website is built, you should be able to see it in the R-studio browser. There is a little button (blue arrow with a little browser icon) that allows you to pop the website into your default web-browser. This way you can look at the website in your browser.

**Important**: If you want to see the website, you need to upload it to a web server to serve the webpage on the internet. Open the main Quarto file (such as index.qmd) in R-Studio, then click render the website by clicking the "Render Website" button in the top right corner of the editor or by running quarto::quarto_render() in the R console.
------------------------------------------------------------------------

### 2. Understanding the Project Structure

Here's an overview of the project's structure:

1. **Main Directories**:
   - **`R-Crash-Course`**: Contains resources and scripts for a crash course in R programming, likely intended to help users familiarize themselves with R for remote sensing applications.
   - **`RESEDA`**: This directory appears to house the core project files and scripts relevant to the RESEDA project.
   - **`_freeze`**, **`docs`**, **`html`**, **`img`**, **`projects`**, **`staff`**: These directories contain various assets such as documentation, HTML files, images, project-specific files, and staff-related information.

2. **Configuration and Setup Files**:
   - **`.gitignore`**: Specifies which files and directories Git should ignore.
   - **`_quarto.yml`**: Configuration file for the Quarto framework, used for rendering the website and documents.
   - **`quarto-website-template.Rproj`**: An R project file template for setting up the Quarto website.

3. **Content Files**:
   - **`index.qmd`**: The main Quarto markdown file that likely serves as the homepage for the website.
   - **`404.qmd`**: A custom 404 error page file.

4. **Other Assets**:
   - **`bootstrap.css`**: CSS file for styling the website, indicating the use of Bootstrap framework for design consistency.

The project is hosted on GitHub, and more details, including the full directory structure and files, can be explored directly on its [GitHub page](https://github.com/Remote-Sensing-at-Fu-Berlin/RESEDA)【13†source】【14†source】【15†source】.

------------------------------------------------------------------------

### 3. Editing Content

**Instructions for Editing Quarto Website Files**


#### **Basic Markdown**
Markdown is a lightweight markup language for creating formatted text using a plain-text editor. Here’s a quick reference:

- **Headings**:
  ```markdown
  # Heading 1
  ## Heading 2
  ### Heading 3
  ```

- **Lists**:
  - **Unordered list**:
    ```markdown
    - Item 1
    - Item 2
      - Subitem 2.1
    ```
  - **Ordered list**:
    ```markdown
    1. First item
    2. Second item
    ```

- **Links**:
  ```markdown
  [Link Text](http://example.com)
  ```

- **Images**:
  ```markdown
  ![Alt Text](http://url/to/image.jpg)
  ```

#### **Quarto Extensions**

Quarto extends Markdown with additional capabilities specific to scientific and technical writing. Some common Quarto-specific syntax and extensions include:

1. **Code Blocks with Output**:
   ```markdown
   ```{r}
   # R code here
   summary(cars)
   ```
   ```

2. **Cross-referencing**:
   ```markdown
   See Figure @fig-plot for details.
   ```

3. **Bibliographies and Citations**:
   ```markdown
   --- 
   bibliography: references.bib 
   ---
   
   Citing a source [@doe2020].
   ```

4. **Layout Elements**:
   - **Columns**:
     ```markdown
     ::: {.column}
     Content in a column.
     :::
     ```

5. **Callouts**:
   ```markdown
   ::: {.callout-note}
   This is a note.
   :::

   ```
To make changes to the RESEDA website, here are the files you should edit based on the type of modification you want to make:

#### **Style Changes**
To change the style of the website, such as modifying the appearance of text, colors, or layout, you should edit the CSS files:

- **`styles/bootstrap.css`**: This file contains the Bootstrap CSS framework and custom styles. Modify this file to adjust the global styles of the website.

#### **Structure Changes**
To change the structure of the website, such as altering the layout of pages or adding new sections, you should edit the Quarto configuration and layout files:

- **`_quarto.yml`**: This configuration file defines the structure and settings for the Quarto project. Modify this file to change site-wide settings, navigation menus, and other structural elements.
- **`index.qmd`**: The main content file that often serves as the homepage. Edit this file to change the structure of the homepage or main content layout.
- **Other `.qmd` files**: Modify other Quarto markdown files in the project (e.g., those in the `docs`, `projects`, or `R-Crash-Course` directories) to change the structure and content of specific sections or pages of the website.

#### **Basic Edits**
For basic edits, such as updating text, images, or adding new content, you should also edit the Quarto markdown files:

- **`index.qmd`**: Edit this file for changes to the homepage content.
- **Other `.qmd` files**: Modify these files to update content in specific sections or pages. For example, updating the course materials in the `R-Crash-Course` directory or project descriptions in the `projects` directory.
- **Images**: Add or replace images in the `img` directory and update the corresponding paths in the markdown files where the images are used.

By editing these files, you can customize the style, structure, and content of the RESEDA website according to your needs. For more detailed instructions on Quarto-specific configurations and markdown syntax, refer to the [Quarto documentation](https://quarto.org/docs/).


------------------------------------------------------------------------

### 4. Publishing Updates

To publish changes to your Quarto website using GitHub Desktop and RStudio, follow these steps:

**Using GitHub Desktop**

1. **Open GitHub Desktop**:
   - Launch GitHub Desktop on your computer.

2. **Clone the Repository** (if not already done):
   - Go to **File > Clone Repository**.
   - Select the repository from your GitHub account and clone it to your local machine.

3. **Make Changes**:
   - Navigate to the cloned repository on your computer and make the necessary changes to your `.qmd` files, CSS files, or configuration files using a text editor (e.g., VS Code) or RStudio.

4. **Commit Changes**:
   - Open GitHub Desktop.
   - You should see the changed files listed in the left pane.
   - Enter a summary of the changes in the "Summary" box.
   - Optionally, add a more detailed description in the "Description" box.
   - Click the **Commit to main** (or the relevant branch) button.

5. **Push Changes**:
   - Click the **Push origin** button at the top to push your committed changes to the GitHub repository.

**Using RStudio**

1. **Open RStudio**:
   - Launch RStudio and open your Quarto project.

2. **Edit Files**:
   - Make changes to your Quarto files (e.g., `.qmd`, `_quarto.yml`) directly within RStudio.

3. **Build and Preview**:
   - To ensure your changes look as expected, build and preview the site locally by running:
     ```r
     quarto::quarto_render()
     ```
   - This command generates the site files and lets you preview them.

4. **Commit Changes**:
   - Use the Git pane in RStudio to commit your changes.
   - In the Git pane, you will see a list of changed files. Check the boxes next to the files you want to commit.
   - Click the **Commit** button.
   - Enter a commit message in the dialog that appears and click **Commit**.

5. **Push Changes**:
   - After committing, click the **Push** button in the Git pane to push your changes to the GitHub repository.


By following these steps, you can efficiently manage and publish your Quarto website changes using both GitHub Desktop and RStudio. The workflow involves making the necessary edits, committing the changes to the local repository, and pushing the updates to the remote GitHub repository. This ensures that your changes are version-controlled and shared with collaborators or published online. For more detailed instructions, refer to the [GitHub Desktop documentation](https://docs.github.com/en/desktop) and the [RStudio Git integration guide](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN).


------------------------------------------------------------------------

### 5. Additional Resources

-   **Links**:
    -   Quarto Documentation: [Quarto Documentation](https://quarto.org/docs/)
    -   Markdown Guide: [Markdown Guide](https://www.markdownguide.org/)
-   **Contact Information**:
    -   In case of trouble, don't hesitate to send an [e-mail](linamapg@gmail.com).

