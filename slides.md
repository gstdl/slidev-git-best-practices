---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: pexels-spacex-586019.jpg
# some information about your slides (markdown enabled)
title: "Git Best Practices"
info: "Git best practices for GitHub and Azure DevOps"
# apply unocss classes to the current slide
class: text-left
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: fade-out
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Git Best Practices
## For GitHub and Azure DevOps

<!--
Comprehensive guide to Git best practices for modern development workflows
-->

---
transition: fade-out
---

# Why Git Best Practices Matter

<div class="absolute top-1/2 transform -translate-y-1/2">

- <span class="text-highlight">Maintain clean and readable project history</span> for better collaboration
- <span class="text-highlight">Enable efficient code reviews</span> and faster debugging
- <span class="text-highlight">Reduce merge conflicts</span> and integration issues
- <span class="text-highlight">Facilitate easier rollbacks</span> and hotfix deployments
- <span class="text-highlight">Support automated CI/CD pipelines</span> and deployment strategies
- <span class="text-highlight">Improve team productivity</span> and code quality

</div>

<style>
h1 {
  background-color: #2B90B6;
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Repository Setup & Configuration

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Initial Setup</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono">
        git config user.name "Your Name"<br>
        git config user.email "your@email.com"
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Essential .gitignore</span></h3>
    <div class="text-sm space-y-2">
        <div class="bg-gray-100 p-2 rounded font-mono text-xs">
          # Common files to ignore<br>
          node_modules/<br>
          .env<br>
          dist/<br>
          *.log<br>
          .DS_Store<br>
          .venv/
        </div>
        <h4 class="text-sm font-bold mt-3 mb-2">Useful Resources:</h4>
        <ul class="text-xs space-y-1">
          <li><a href="https://github.com/github/gitignore/blob/main/Python.gitignore" target="_blank" class="text-blue-600 hover:text-blue-800 underline">Python .gitignore template</a></li>
          <li><a href="https://www.toptal.com/developers/gitignore" target="_blank" class="text-blue-600 hover:text-blue-800 underline">gitignore.io generator</a></li>
        </ul>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Sample Repository Structure</span></h3>
    <div class="text-sm space-y-1">
      <div>📄 <strong>README.md</strong> - Project overview and setup</div>
      <div>📄 <strong>CONTRIBUTING.md</strong> - Contribution guidelines</div>
      <div>📁 <strong>.github/</strong> - GitHub templates and workflows</div>
      <div>📁 <strong>.git/</strong> - Git configuration and hooks</div>
      <div>📁 <strong>docs/</strong> - Documentation</div>
      <div>📁 <strong>scripts/</strong> - Build and deployment scripts</div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Branch Protection</span></h3>
    <div class="text-sm space-y-1">
      <div>✅ Require pull request reviews</div>
      <div>✅ Require status checks to pass</div>
      <div>✅ Restrict pushes to main branch</div>
      <div>✅ Include administrators in restrictions</div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Branching Strategies

<div class="grid grid-cols-3 gap-6">
  <div class="bg-blue-50 p-4 rounded-lg">
    <h3 class="font-bold text-blue-600 mb-3">🌊 Git Flow</h3>
    <div class="text-sm space-y-2">
      <div><strong>main:</strong> Production releases</div>
      <div><strong>develop:</strong> Integration branch</div>
      <div><strong>feature/*:</strong> New features</div>
      <div><strong>release/*:</strong> Release preparation</div>
      <div><strong>hotfix/*:</strong> Critical fixes</div>
    </div>
    <div class="mt-3 text-xs bg-blue-100 p-2 rounded">
      <strong>Best for:</strong> Complex projects with scheduled releases
    </div>
  </div>

  <div class="bg-green-50 p-4 rounded-lg">
    <h3 class="font-bold text-green-600 mb-3">🚀 GitHub Flow</h3>
    <div class="text-sm space-y-2">
      <div><strong>main:</strong> Always deployable</div>
      <div><strong>feature/*:</strong> All development</div>
      <div><strong>Process:</strong></div>
      <div class="ml-2">1. Create branch from main</div>
      <div class="ml-2">2. Develop & commit</div>
      <div class="ml-2">3. Open pull request</div>
      <div class="ml-2">4. Review & merge</div>
    </div>
    <div class="mt-3 text-xs bg-green-100 p-2 rounded">
      <strong>Best for:</strong> Continuous deployment, web apps
    </div>
  </div>

  <div class="bg-purple-50 p-4 rounded-lg">
    <h3 class="font-bold text-purple-600 mb-3">🔄 GitLab Flow</h3>
    <div class="text-sm space-y-2">
      <div><strong>main:</strong> Development</div>
      <div><strong>production:</strong> Live environment</div>
      <div><strong>staging:</strong> Testing environment</div>
      <div><strong>feature/*:</strong> Feature development</div>
    </div>
    <div class="mt-3 text-xs bg-purple-100 p-2 rounded">
      <strong>Best for:</strong> Multiple environments, staged deployments
    </div>
  </div>
</div>

<div class="mt-6 bg-yellow-50 p-4 rounded-lg">
  <h3 class="font-bold text-yellow-600 mb-2">💡 Branch Naming Conventions</h3>
  <div class="grid grid-cols-2 gap-4 text-sm">
    <div>
      <div class="font-mono bg-gray-100 p-1 rounded">feature/user-authentication</div>
      <div class="font-mono bg-gray-100 p-1 rounded mt-1">bugfix/login-validation-error</div>
      <div class="font-mono bg-gray-100 p-1 rounded mt-1">hotfix/security-patch-2024</div>
    </div>
    <div>
      <div class="font-mono bg-gray-100 p-1 rounded">release/v2.1.0</div>
      <div class="font-mono bg-gray-100 p-1 rounded mt-1">chore/update-dependencies</div>
      <div class="font-mono bg-gray-100 p-1 rounded mt-1">docs/api-documentation</div>
    </div>
  </div>
</div>

---
transition: fade-out
---

# Commit Message Best Practices

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Conventional Commits</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        &lt;type&gt;[optional scope]: &lt;description&gt;<br><br>
        [optional body]<br><br>
        [optional footer(s)]
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Commit Types</span></h3>
    <div class="text-sm space-y-1">
      <div><strong>feat:</strong> New feature</div>
      <div><strong>fix:</strong> Bug fix</div>
      <div><strong>docs:</strong> Documentation changes</div>
      <div><strong>style:</strong> Code formatting</div>
      <div><strong>refactor:</strong> Code restructuring</div>
      <div><strong>test:</strong> Adding tests</div>
      <div><strong>chore:</strong> Maintenance tasks</div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Good Examples</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-green-100 p-2 rounded font-mono text-xs">
        feat(auth): add OAuth 2.0 integration<br><br>
        - Implement Google OAuth provider<br>
        - Add user session management<br>
        - Update login UI components<br><br>
        Closes #123
      </div>
      <div class="bg-green-100 p-2 rounded font-mono text-xs">
        fix(api): resolve timeout in user endpoint<br><br>
        Increase timeout from 5s to 30s for large datasets
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Bad Examples</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-red-100 p-2 rounded font-mono text-xs">
        ❌ update stuff<br>
        ❌ fix bug<br>
        ❌ WIP<br>
        ❌ final version
      </div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# GitHub Best Practices

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Pull Request Workflow</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Create feature branch<br>
        git checkout -b feature/new-dashboard<br><br>
        # Make changes and commit<br>
        git add .<br>
        git commit -m "feat: add user dashboard"<br><br>
        # Push and create PR<br>
        git push origin feature/new-dashboard
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">PR Templates</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        ## Description<br>
        Brief description of changes<br><br>
        ## Type of Change<br>
        - [ ] Bug fix<br>
        - [ ] New feature<br>
        - [ ] Breaking change<br><br>
        ## Testing<br>
        - [ ] Unit tests pass<br>
        - [ ] Integration tests pass
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">GitHub Actions Example</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        name: CI/CD Pipeline<br><br>
        on:<br>
        &nbsp;&nbsp;pull_request:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;branches: [ main ]<br>
        &nbsp;&nbsp;push:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;branches: [ main ]<br><br>
        jobs:<br>
        &nbsp;&nbsp;test:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;runs-on: ubuntu-latest<br>
        &nbsp;&nbsp;&nbsp;&nbsp;steps:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;- uses: actions/checkout@v3<br>
        &nbsp;&nbsp;&nbsp;&nbsp;- name: Run tests<br>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;run: npm test
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Issue Templates</span></h3>
    <div class="text-sm space-y-1">
      <div>🐛 <strong>Bug Report Template</strong></div>
      <div>✨ <strong>Feature Request Template</strong></div>
      <div>❓ <strong>Question Template</strong></div>
      <div>🔧 <strong>Task Template</strong></div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Azure DevOps Best Practices

<div class="grid grid-cols-2 grid-rows-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Azure Repos Setup</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Clone Azure DevOps repo<br>
        git clone https://dev.azure.com/org/project/_git/repo<br><br>
        # Set up remote tracking<br>
        git remote add origin https://dev.azure.com/org/project/_git/repo<br><br>
        # Configure for Azure DevOps<br>
        git config credential.helper manager-core
      </div>
    </div>
    <div class="text-sm space-y-1">
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Branch Policies</span></h3>
      <div>✅ Require minimum 2 reviewers</div>
      <div>✅ Check for linked work items</div>
      <div>✅ Require build validation</div>
      <div>✅ Auto-complete after requirements met</div>
      <div>✅ Squash merge for clean history</div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Azure Pipelines YAML</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        trigger:<br>
        - main<br>
        - develop<br><br>
        pr:<br>
        - main<br><br>
        pool:<br>
        &nbsp;&nbsp;vmImage: 'ubuntu-latest'<br><br>
        steps:<br>
        - task: NodeTool@0<br>
        &nbsp;&nbsp;inputs:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;versionSpec: '18.x'<br><br>
        - script: npm ci<br>
        &nbsp;&nbsp;displayName: 'Install dependencies'<br><br>
        - script: npm test<br>
        &nbsp;&nbsp;displayName: 'Run tests'
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Work Item Integration</span></h3>
    <div class="text-sm space-y-1">
      <div>🔗 Link commits to work items</div>
      <div>📋 Reference work items in PR descriptions</div>
      <div>🎯 Use AB# prefix for automatic linking</div>
      <div>✅ Close work items via commits</div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Code Review Best Practices

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Before Submitting PR</span></h3>
    <div class="text-sm space-y-2">
      <div>✅ <strong>Self-review your code</strong></div>
      <div>✅ <strong>Run tests locally</strong></div>
      <div>✅ <strong>Update documentation</strong></div>
      <div>✅ <strong>Add meaningful commit messages</strong></div>
      <div>✅ <strong>Keep PRs small and focused</strong></div>
      <div>✅ <strong>Include screenshots for UI changes</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">PR Description Template</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        ## What changed?<br>
        Brief summary of the changes<br><br>
        ## Why?<br>
        Explain the motivation<br><br>
        ## How to test?<br>
        Step-by-step testing instructions<br><br>
        ## Screenshots<br>
        Before/after images if applicable
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">During Code Review</span></h3>
    <div class="text-sm space-y-2">
      <div>👀 <strong>Review logic and architecture</strong></div>
      <div>🔍 <strong>Check for security vulnerabilities</strong></div>
      <div>📝 <strong>Verify code readability</strong></div>
      <div>⚡ <strong>Assess performance impact</strong></div>
      <div>🧪 <strong>Ensure adequate test coverage</strong></div>
      <div>📚 <strong>Validate documentation updates</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Review Comments</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-green-100 p-2 rounded">
        <div class="font-bold text-green-600">✅ Good:</div>
        <div>"Consider using a Map here for O(1) lookup instead of Array.find() for better performance"</div>
      </div>
      <div class="bg-red-100 p-2 rounded">
        <div class="font-bold text-red-600">❌ Bad:</div>
        <div>"This is wrong"</div>
      </div>
    </div>
  </div>
</div>

```mermaid
sequenceDiagram
  Alice->John: Hello John, how are you?
  Note over Alice,John: A typical interaction
```

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Advanced Git Techniques

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Interactive Rebase</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Clean up commit history<br>
        git rebase -i HEAD~3<br><br>
        # Options:<br>
        # pick - keep commit<br>
        # squash - combine with previous<br>
        # edit - modify commit<br>
        # drop - remove commit
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Git Hooks</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # .git/hooks/pre-commit<br>
        #!/bin/sh<br>
        npm run lint<br>
        npm run test<br><br>
        # .git/hooks/commit-msg<br>
        #!/bin/sh<br>
        # Validate commit message format<br>
        npx commitlint --edit $1
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Cherry-picking</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Apply specific commit to current branch<br>
        git cherry-pick &lt;commit-hash&gt;<br><br>
        # Apply multiple commits<br>
        git cherry-pick A..B<br><br>
        # Cherry-pick without committing<br>
        git cherry-pick --no-commit &lt;hash&gt;
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Bisect for Debugging</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Start bisect session<br>
        git bisect start<br>
        git bisect bad HEAD<br>
        git bisect good &lt;known-good-commit&gt;<br><br>
        # Git will checkout middle commit<br>
        # Test and mark as good/bad<br>
        git bisect good  # or git bisect bad<br><br>
        # Finish when bug is found<br>
        git bisect reset
      </div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Security & Compliance

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Secure Practices</span></h3>
    <div class="text-sm space-y-2">
      <div>🔐 <strong>Never commit secrets</strong></div>
      <div>🎯 <strong>Use .gitignore for sensitive files</strong></div>
      <div>🔑 <strong>Use SSH keys or Personal Access Tokens</strong></div>
      <div>🛡️ <strong>Enable 2FA on all accounts</strong></div>
      <div>🔍 <strong>Scan for secrets in commits</strong></div>
      <div>📝 <strong>Sign commits with GPG</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Secret Scanning</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Install git-secrets<br>
        brew install git-secrets<br><br>
        # Set up for repository<br>
        git secrets --install<br>
        git secrets --register-aws<br><br>
        # Scan commits<br>
        git secrets --scan
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Compliance & Audit</span></h3>
    <div class="text-sm space-y-2">
      <div>📊 <strong>Enable audit logging</strong></div>
      <div>👥 <strong>Track contributor activity</strong></div>
      <div>🔒 <strong>Enforce branch protection rules</strong></div>
      <div>📋 <strong>Maintain compliance documentation</strong></div>
      <div>🔄 <strong>Regular access reviews</strong></div>
      <div>📈 <strong>Monitor repository metrics</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">GitHub Security Features</span></h3>
    <div class="text-sm space-y-2">
      <div>🔍 <strong>Dependabot alerts</strong></div>
      <div>🛡️ <strong>Security advisories</strong></div>
      <div>🔐 <strong>Secret scanning</strong></div>
      <div>📝 <strong>Code scanning with CodeQL</strong></div>
      <div>🎯 <strong>Dependency review</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Azure DevOps Security</span></h3>
    <div class="text-sm space-y-2">
      <div>🔑 <strong>Azure AD integration</strong></div>
      <div>🛡️ <strong>Conditional access policies</strong></div>
      <div>📊 <strong>Audit trail and reporting</strong></div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Release Management

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Semantic Versioning</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono">
        <div class="text-center text-lg">MAJOR.MINOR.PATCH</div>
        <div class="text-center text-lg">2.1.3</div>
      </div>
      <div>🔴 <strong>MAJOR:</strong> Breaking changes</div>
      <div>🟡 <strong>MINOR:</strong> New features (backward compatible)</div>
      <div>🟢 <strong>PATCH:</strong> Bug fixes</div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Git Tags</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Create annotated tag<br>
        git tag -a v2.1.0 -m "Release version 2.1.0"<br><br>
        # Push tags to remote<br>
        git push origin --tags<br><br>
        # List tags<br>
        git tag -l
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">GitHub Releases</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Using GitHub CLI<br>
        gh release create v2.1.0 \<br>
        &nbsp;&nbsp;--title "Version 2.1.0" \<br>
        &nbsp;&nbsp;--notes "## What's New<br>
        &nbsp;&nbsp;- Feature A<br>
        &nbsp;&nbsp;- Bug fix B" \<br>
        &nbsp;&nbsp;dist/*
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Azure DevOps Releases</span></h3>
    <div class="text-sm space-y-2">
      <div>🚀 <strong>Release pipelines</strong></div>
      <div>🎯 <strong>Multi-stage deployments</strong></div>
      <div>✅ <strong>Approval gates</strong></div>
      <div>📋 <strong>Release notes automation</strong></div>
      <div>🔄 <strong>Rollback strategies</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Changelog Automation</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Generate changelog<br>
        npx conventional-changelog-cli -p angular -i CHANGELOG.md -s<br><br>
        # With release automation<br>
        npx semantic-release
      </div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Common Git Problems & Solutions

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Merge Conflicts</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # When merge conflict occurs<br>
        git status  # See conflicted files<br><br>
        # Edit files to resolve conflicts<br>
        # Look for &lt;&lt;&lt;&lt;&lt;&lt;&lt; markers<br><br>
        # After resolving<br>
        git add .<br>
        git commit -m "resolve merge conflicts"
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Undo Changes</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Undo last commit (keep changes)<br>
        git reset --soft HEAD~1<br><br>
        # Undo last commit (discard changes)<br>
        git reset --hard HEAD~1<br><br>
        # Undo specific file<br>
        git checkout -- filename.js
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Large File Issues</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Install Git LFS<br>
        git lfs install<br><br>
        # Track large files<br>
        git lfs track "*.psd"<br>
        git lfs track "*.zip"<br><br>
        # Commit .gitattributes<br>
        git add .gitattributes<br>
        git commit -m "track large files with LFS"
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Repository Cleanup</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Remove file from history<br>
        git filter-branch --force --index-filter \<br>
        'git rm --cached --ignore-unmatch secrets.env' \<br>
        --prune-empty --tag-name-filter cat -- --all<br><br>
        # Alternative with BFG<br>
        java -jar bfg.jar --delete-files secrets.env<br>
        git reflog expire --expire=now --all<br>
        git gc --prune=now --aggressive
      </div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Performance & Optimization

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Repository Performance</span></h3>
    <div class="text-sm space-y-2">
      <div>📦 <strong>Keep repository size manageable</strong></div>
      <div>🗂️ <strong>Use Git LFS for large files</strong></div>
      <div>🧹 <strong>Regular garbage collection</strong></div>
      <div>📈 <strong>Monitor repository metrics</strong></div>
      <div>🔍 <strong>Analyze repository with git-sizer</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Git Configuration</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # Optimize for performance<br>
        git config core.preloadindex true<br>
        git config core.fscache true<br>
        git config gc.auto 256<br><br>
        # Enable parallel processing<br>
        git config pack.threads 0<br><br>
        # Use SSH multiplexing<br>
        git config core.sshCommand "ssh -o ControlMaster=auto -o ControlPersist=600s"
      </div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Workflow Optimization</span></h3>
    <div class="text-sm space-y-2">
      <div>⚡ <strong>Use shallow clones for CI</strong></div>
      <div>🎯 <strong>Optimize pipeline triggers</strong></div>
      <div>📦 <strong>Cache dependencies</strong></div>
      <div>🔄 <strong>Parallel job execution</strong></div>
      <div>📊 <strong>Monitor build performance</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">CI/CD Optimization</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded font-mono text-xs">
        # GitHub Actions optimization<br>
        - uses: actions/checkout@v3<br>
        &nbsp;&nbsp;with:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;fetch-depth: 1  # Shallow clone<br><br>
        # Cache node modules<br>
        - uses: actions/cache@v3<br>
        &nbsp;&nbsp;with:<br>
        &nbsp;&nbsp;&nbsp;&nbsp;path: ~/.npm<br>
        &nbsp;&nbsp;&nbsp;&nbsp;key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
      </div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Monitoring</span></h3>
    <div class="text-sm space-y-2">
      <div>📈 <strong>Track repository size growth</strong></div>
      <div>⏱️ <strong>Monitor clone/fetch times</strong></div>
      <div>🔍 <strong>Analyze commit patterns</strong></div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Team Collaboration Best Practices

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Team Workflows</span></h3>
    <div class="text-sm space-y-2">
      <div>📋 <strong>Establish clear Git workflows</strong></div>
      <div>📝 <strong>Document branching strategy</strong></div>
      <div>👥 <strong>Define code review process</strong></div>
      <div>🎯 <strong>Set merge/PR requirements</strong></div>
      <div>📊 <strong>Regular retrospectives</strong></div>
      <div>🔄 <strong>Continuous improvement</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Communication</span></h3>
    <div class="text-sm space-y-2">
      <div>💬 <strong>Clear PR descriptions</strong></div>
      <div>🏷️ <strong>Meaningful commit messages</strong></div>
      <div>📋 <strong>Link to issue tracking</strong></div>
      <div>📚 <strong>Update documentation</strong></div>
      <div>🔔 <strong>Timely PR reviews</strong></div>
      <div>❓ <strong>Ask questions when unclear</strong></div>
    </div>
  </div>
  
  <div>
    <h3 class="text-lg font-bold mb-4"><span class="text-highlight">Onboarding New Developers</span></h3>
    <div class="text-sm space-y-2">
      <div>📖 <strong>Git workflow documentation</strong></div>
      <div>🛠️ <strong>Setup scripts and guides</strong></div>
      <div>👨‍🏫 <strong>Pair programming sessions</strong></div>
      <div>📝 <strong>Code review training</strong></div>
      <div>🎯 <strong>Practice repositories</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Knowledge Sharing</span></h3>
    <div class="text-sm space-y-2">
      <div>📚 <strong>Maintain team wiki</strong></div>
      <div>🎤 <strong>Regular tech talks</strong></div>
      <div>💡 <strong>Share Git tips & tricks</strong></div>
      <div>🏆 <strong>Celebrate good practices</strong></div>
      <div>🔍 <strong>Code review feedback</strong></div>
    </div>
    <h3 class="text-lg font-bold mb-4 mt-6"><span class="text-highlight">Quality Gates</span></h3>
    <div class="text-sm space-y-2">
      <div class="bg-gray-100 p-2 rounded">
        <div>✅ All tests pass</div>
        <div>✅ Code coverage threshold met</div>
        <div>✅ Security scans pass</div>
        <div>✅ Performance benchmarks</div>
        <div>✅ Documentation updated</div>
      </div>
    </div>
  </div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
layout: center
class: text-center
---

# Thank You!

## Questions & Discussion

<div class="mt-8">
<h3 class="text-lg font-bold"><span class="text-highlight">Key Takeaways</span></h3>
<ul class="mt-4 text-sm list-none">
  <li>🌊 Choose the right branching strategy for your team and project</li>
  <li>📝 Write clear, conventional commit messages for better history</li>
  <li>🔍 Implement thorough code review processes</li>
  <li>🛡️ Prioritize security and compliance in your Git workflows</li>
  <li>⚡ Optimize performance for large repositories and teams</li>
  <li>👥 Foster collaboration through clear documentation and communication</li>
</ul>
</div>

<div class="mt-8 text-sm">
<div class="font-bold">📚 Additional Resources:</div>
<div>• Pro Git Book (git-scm.com/book)</div>
<div>• GitHub Docs & Azure DevOps Documentation</div>
<div>• Conventional Commits (conventionalcommits.org)</div>
</div>

<style>
.text-highlight {
  background-color: #2B90B6;
  background-size: 100%;
  font-weight: bold;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

