# renovate-config

## Presets

### default.jsonc

#### config:recommended

```json
{
  "extends": [
    ":dependencyDashboard", 
    ":semanticPrefixFixDepsChoreOthers", 
    ":ignoreModulesAndTests", 
    "group:monorepos", 
    "group:recommended", 
    "mergeConfidence:age-confidence-badges", 
    "replacements:all", 
    "workarounds:all", 
    "security:php2shell", 
    "helpers:forgejoDigestChangelogs", 
    "helpers:giteaDigestChangelogs", 
    "helpers:githubDigestChangelogs", 
    "helpers:gitlabDigestChangelogs", 
    "helpers:goXPackagesChangelogLink", 
    "helpers:goXPackagesNameLink", 
    "helpers:renovateChangelog" 
  ]
}
```

#### config:best-practices

```json
{
  "extends": [
    "config:recommended", 
    "docker:pinDigests", 
    "helpers:pinGitHubActionDigests", 
    ":configMigration", 
    ":pinDevDependencies", 
    "abandonments:recommended", 
    "security:minimumReleaseAgeNpm", 
    ":maintainLockFilesWeekly" 
  ]
}
```

#### schedule:monthly

```json
{
  "schedule": [
    "*0-3 1* *"
  ]
}
```

#### schedule:automergeEarlyMondays

```json
{
  "automergeSchedule": [
    "* 0-3 * * 1"
  ]
}
```

#### :automergeBranch

```json
{
  "automergeType": "branch"
}
```

#### :automergeRequireAllStatusChecks

```json
{
  "ignoreTests": false
}
```
