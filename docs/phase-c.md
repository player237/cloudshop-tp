# Phase C — Week 5 (DevOps pipeline)

## Your pipeline diagram

```
Local code → git push → GitHub Actions → tests → docker build
```

State: where does it **stop** if a test fails? What stays **manual** in your setup?

State: The pipeline STOPS at the 'Tests' step if any test fails. This prevents broken code from reaching production.

What stays manual: Deciding when to merge a pull request, reviewing code, the deployment to a server

## Questions

1. DevOps in one sentence:

 DevOps is a set of practices that unites software development (Dev) and operations (Ops) teams to automate and accelerate the delivery of software while maintaining quality and reliability.

2. Two measurable DevOps goals:

•Reduce deployment time: instead of deploying manually once a month, automate to deploy multiple times per day.

•Reduce failure rate: use automated tests in CI to catch bugs before they reach users.

3. What remains manual in **your** lab:

•Code review and pull request approval; a human decides if code is ready to merge.

•Writing and updating tests; automation only runs tests; a developer must write them.
