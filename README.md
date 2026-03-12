# TB Case Management Staffing Calculator

A duration-adjusted workforce planning tool for tuberculosis case management programs, developed for DPHN (District Public Health Nursing) teams.

---

## Features

- **Duration-adjusted case weightings** using the case-months methodology (duration × care intensity per case type)
- - **Contact investigation workload modeling** with separate components for CI administrative overhead and per-contact direct work
  - - **Cross-coverage buffer calculations** for vacancies and planned leave
    - - **Real-time staffing recommendations** and capacity utilization display
      - - **Single self-contained HTML file** — no build step, no dependencies
       
        - ---

        ## Usage

        ### Run Locally

        Open `index.html` in any web browser. No server or installation required.

        ### Deploy to GitHub Pages

        1. Create a new repository on GitHub
        2. 2. Upload `index.html` to the repository
           3. 3. Go to **Settings → Pages**
              4. 4. Set **Source** to the `main` branch, root folder (`/`)
                 5. 5. Your tool will be live at:
                    6.    ```
                             https://yourusername.github.io/repositoryname/
                             ```

                          ---

                      ## Methodology

                    Each case type contributes a **case-month weight** calculated as:

                    > **Case-Month Weight** = Average Duration (months) × Care Intensity Multiplier
                    >
                    > Contact investigations (CIs) add two components:
                    > - An **administrative overhead** per CI
                    > - - A **direct-work weight** per individual contact
                    >  
                    >   - Total weighted workload is divided by the per-nurse annual target to determine baseline FTE need. A **cross-coverage buffer** is then applied on top to account for vacancies and leave.
                    >  
                    >   - ### Default Case Type Parameters
                    >  
                    >   - | Case Type      | Default Duration | Default Intensity | Case-Month Weight |
                    >   - |----------------|-----------------|-------------------|-------------------|
                    >   - | TB3 Complex    | 8 months        | 3.0               | 24.0              |
                    >   - | TB3 Routine    | 6 months        | 1.5               | 9.0               |
                    >   - | TB5 with Meds  | 3 months        | 1.0               | 3.0               |
                    >
                    >   - > All parameters are editable directly within the tool.
                    >     >
                    >     > ---
                    >     >
                    >     > ## Author
                    >     >
                    >     > Developed for the **LA County Department of Public Health — Medical and Dental Affairs**.
