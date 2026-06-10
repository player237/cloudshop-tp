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

1. Week 1:
2. Week 2:
3. Week 3:
4. Week 4:
5. Week 5:
6. Week 6:
7. Week 7:

**Automation:** what happens when you `git push`?

**Without AWS:** what did you simulate instead?

## AWS bonus (optional)

(If applicable: IP, screenshots, instance termination date)
