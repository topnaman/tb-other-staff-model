TB Case Management Staffing Calculator
A duration-adjusted DPHN workforce planning tool for tuberculosis case management programs.
Features
Duration-adjusted case weightings using the case-months methodology (duration × care intensity per case type)
Contact investigation workload modeling with separate CI-admin and per-contact components
Cross-coverage buffer calculations for vacancies and leave
Real-time staffing recommendations and capacity utilization
Single self-contained HTML file — no build step, no dependencies
Usage
Open `index.html` in any web browser. No server required.
Deploy to GitHub Pages
Create a new repository on GitHub
Upload `index.html`
Go to Settings → Pages
Set Source to `main` branch, root folder
Your tool will be live at `https://yourusername.github.io/repositoryname/`
Methodology
Each case type contributes a case-month weight = average duration (months) × care intensity multiplier. Contact investigations add two components: an administrative overhead per CI and a direct-work weight per individual contact. Total weighted workload divided by the per-nurse annual target gives baseline FTE need; a cross-coverage buffer is applied on top.
Case Type	Default Duration	Default Intensity	Case-Month Weight
TB3 Complex	8 mo	3.0	24.0
TB3 Routine	6 mo	1.5	9.0
TB5 with Meds	3 mo	1.0	3.0
All parameters are editable in the tool.
Author
Developed for LA County Department of Public Health — Medical and Dental Affairs
