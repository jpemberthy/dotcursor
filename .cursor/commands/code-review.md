# Code Review

Review the changes on @branch:

- Think through how data flows in the app. Explain new patterns if they exist and why.
- Were there any changes that could affect infrastructure?
- Consider empty, loading, error, and offline states.
- Did we add any unnecessary dependencies? If there's a heavy dependency, could we inline a more minimal version?
- Were there schema changes which could require a database migration?
- Are there tests that can be more explicitly written? If so, write them.