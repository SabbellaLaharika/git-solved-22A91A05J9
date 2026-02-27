# My Git Mastery Challenge Journey

## Student Information
- **Name**: Sabbella Laharika
- **Student ID**: 22A91A05J9
- **Repository**: https://github.com/SabbellaLaharika/git-solved-22A91A05J9
- **Date Started**: 2026-02-27
- **Date Completed**: 2026-02-27

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all
merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|---------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 2 | Copy specific commits |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |
| git reflog | 1 | Recover lost commits |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used port 8080, development used 3000
- **Resolution**: Created unified config with environment-based settings
- **Strategy**: Keep production as default, add dev as optional
- **Difficulty**: Medium

#### Conflict 2: config/database-config.json
- **Issue**: Different database hosts and SSL modes
- **Resolution**: Created separate profiles for production and development
- **Strategy**: Restructured JSON to support both environments
- **Difficulty**: Medium

#### Conflict 3: scripts/deploy.sh
- **Issue**: Different deployment strategies (production vs docker-compose)
- **Resolution**: Added conditional logic based on DEPLOY_ENV variable
- **Strategy**: Made script handle both environments dynamically
- **Difficulty**: Hard

#### Conflict 4: scripts/monitor.js
- **Issue**: Different monitoring intervals and log formats
- **Resolution**: Environment-based configuration object
- **Strategy**: Used process.env.NODE_ENV to determine behavior
- **Difficulty**: Medium

#### Conflict 5: docs/architecture.md
- **Issue**: Different architectural descriptions for each env
- **Resolution**: Merged both descriptions into comprehensive document
- **Strategy**: Created sections for each environment
- **Difficulty**: Easy

#### Conflict 6: README.md
- **Issue**: Different feature lists and version numbers
- **Resolution**: Combined all features with clear environment labels
- **Strategy**: Organized features by category
- **Difficulty**: Easy

### Merge 2: main + conflict-simulator (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Experimental version (3.0.0) with AI features vs production config
- **Resolution**: Kept production config, added experimental features as commented-out section
- **Strategy**: Production stability first, experimental behind comments/flags
- **Difficulty**: Medium

#### Conflict 2: config/database-config.json
- **Issue**: Distributed multi-node DB config vs production/dev profiles
- **Resolution**: Kept prod/dev profiles, added experimental config as disabled `_experimental_disabled` key
- **Strategy**: Maintain backward compatibility
- **Difficulty**: Medium

#### Conflict 3: scripts/deploy.sh
- **Issue**: AI-powered multi-cloud canary deployment vs multi-env script
- **Resolution**: Kept stable multi-env script, added experimental AI/canary as commented block
- **Strategy**: Experimental features behind EXPERIMENTAL=true flag
- **Difficulty**: Hard

#### Conflict 4: scripts/monitor.js
- **Issue**: AI-enhanced monitoring with ML vs ENV-based monitor
- **Resolution**: Kept ENV-based config, added AI features behind EXPERIMENTAL_AI=true flag
- **Strategy**: Feature flag pattern for experimental code
- **Difficulty**: Hard

#### Conflict 5: docs/architecture.md
- **Issue**: Experimental AI/multi-cloud architecture vs stable docs
- **Resolution**: Kept stable prod/dev docs, added experimental features in clearly marked section
- **Strategy**: Document experimental features as NOT PRODUCTION-READY
- **Difficulty**: Easy

#### Conflict 6: README.md
- **Issue**: Experimental build description vs stable README
- **Resolution**: Kept stable docs, added experimental features list with ⚠️ warning
- **Strategy**: Clearly separate stable from experimental
- **Difficulty**: Easy

## Most Challenging Parts

1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. **Nested Conflicts (Phase 3)**: monitor.js had 3-way conflicts from all three branches, requiring a complete rewrite.

5. **PowerShell Quirks**: `echo >>` in PowerShell writes UTF-16LE causing null byte corruption. Used `Add-Content` and direct file writes instead.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands including reflog and cherry-pick

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- `git reflog` is a lifesaver for recovering lost commits
- Use feature flags to integrate experimental features safely
- `git stash` is essential for context switching

## Reflection
This challenge taught me that merge conflicts aren't scary — they're
just Git asking "which version do you want?". The key is understanding
what each side is trying to do before combining them. I now feel
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and
cherry-pick) was invaluable. I understand the difference between merge
and rebase, and when to use each. Most importantly, I learned that
`git reflog` is a lifesaver when you think you've lost commits!
