# CloudShop Report

**Names:** ABENA OKALA THIERRY

**Date:**10/06/2026  
**GitHub URL:**

## Git history

Paste here:

```
git log --oneline
```

## Phase D — GitHub Actions (PaaS or IaaS?)
•GitHub Actions,the user brings the workflow logic and GitHub brings everything else. That is the definition of PaaS.
(5 lines)

## Phase E — Dockerfile

Explain each line of your Dockerfile (especially why `requirements.txt` is copied before `app.py`)

.WORKDIR /app → Set the working directory inside the container to /app. All following commands will run from this folder.

COPY requirements.txt . → Copy ONLY the requirements file first (before copying the rest of the code).

•requirements.txt rarely changes. So 'pip install' (the next step) will be cached on most builds.

•app.py changes frequently (every time you write code). If you copied it first, every code change would invalidate the pip install layer and force re-downloading all packages — very slow.

## Phase F — Take-home summary

For **each week 1–7**, one sentence: “What I applied concretely”:

1. Week 1: I learned the difference between IaaS, PaaS, and SaaS

2. Week 2: I wrote a Dockerfile for the Flask API and understood why requirements.txt must be copied before app.py for Docker layer caching.

3. Week 3:I set up a GitHub Actions workflow that automatically runs tests and builds the Docker image on every git push.

4. Week 4: I compared AWS, Azure, and GCP services side by side and explained why GitHub Actions (PaaS) is preferred over self-hosting Jenkins (IaaS).

5. Week 5:I understood the full DevOps pipeline from local code to automated CI/CD, identified what remains manual, and wrote a measurable DevOps improvement goal.

6. Week 6:

7. Week 7:

**Automation:** what happens when you `git push`?
When you run git push, Git performs several actions to synchronize your local commits with a remote repository (e.g., on GitHub).

**Without AWS:** what did you simulate instead?

## AWS bonus (optional)

(If applicable: IP, screenshots, instance termination date)
