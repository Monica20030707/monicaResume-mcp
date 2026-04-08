# Resume Customization Workflow

When a job description is provided in `JobDesc.md`, follow these steps to generate a tailored resume:

1.  **Fresh Initialization:**
    -   **Always** start by reading these instructions.
    -   **Never** use customizations, company names, or edits from previous job descriptions. Each run must be a fresh start based solely on `templates/resume_template.tex` and the current `JobDesc.md`.

2.  **Analyze Job Description:**
    -   Extract the company name and key requirements from `JobDesc.md`.
    -   If the company name is missing, use "Custom".

3.  **Template Integrity & Content Selection:**
    -   Use `templates/resume_template.tex` as the base template. **Never modify or overwrite `templates/resume_template.tex`.**
    -   **Content Selection Pool:** All experiences and projects in `templates/resume_template.tex` are available for use, including those currently inside `\begin{comment} ... \end{comment}` blocks.
    -   **Experience Limit:** Select and include exactly **4 experiences** that best match the job description.
    -   **Project Limit:** Select and include exactly **2 projects** that best match the job description.
    -   **Skill Customization:** Modify the "Skills" section (Languages, Skills, Tools) to prioritize keywords from the `JobDesc.md`. Do NOT create new sections; keep the existing three categories.
    -   **One-Page Limit:** Ensure the generated LaTeX code remains within a **single page**. If content is too long, prioritize the most relevant bullet points.
    -   **Formatting:** Maintain the **exact** LaTeX structure, formatting, margins, and style of `templates/resume_template.tex`. Do not change the name, contact info, or education sections unless specifically relevant to the job.

4.  **Generate Customized LaTeX:**
    -   Create a new file using the following naming convention: `resumes/Thuy-<PositionShort>-<Company>-Resume.tex` (e.g., `resumes/Thuy-SDE-Google-Resume.tex`).
    -   Use standard abbreviations for PositionShort: SDE (Software Development Engineer), ADE (Associate Developer/Engineer), SWE (Software Engineer), DS (Data Scientist), etc.
    -   Uncomment selected experiences/projects if they were commented in the original, and comment out the ones not selected.

5.  **GitHub Workflow & PDF Management:**
    -   Ensure a `resumes/` subdirectory exists for `.tex` files and a `pdfs/` subdirectory exists for generated PDFs.
    -   Pushing a new `.tex` file to GitHub will trigger an automated workflow.
    -   The workflow will compile all `.tex` files from the `resumes/` directory and save the resulting PDFs into the `pdfs/` directory.

---
*Note: This workflow is triggered by updates to `JobDesc.md`.*

