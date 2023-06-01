# Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA

https://www.youtube.com/watch?v=O6lr-LKhEwI

https://github.com/RodrigoMvs123/Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA/blob/main/README.md?plain=1

https://github.com/RodrigoMvs123/Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA/blame/main/README.md

Actions Tab.

Yml files.

Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA
Github
Workflow

Actions Tab.
Get started with Github Actions 
Suggested for this repository
Skip this and ( set up a workflow yourself )
Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA/.github/workflows/hello.yml in main


Edit / Preview
name: Display hello, world
on: [workflow_dispatch] 


jobs:
       display-greeting: 
              runs-on: ubuntu latest
              steps:
name: run-echo
run: echo “Hello, world” 


Commit changes 
Actions
Actions 
All workflow
Display hello, world
Run workflow - run workflow
Display hello, world
hello.yml - display-greeting
Set up job


run-echo
Run echo “Hello, world”
Hello, world


Complete job

Code
app.cy.ts ( runs test )

code.
Visual Studio Code 
ReadME.md

Pets workshop
This repository contains the project for both a guided workshop and Modern DevOps with Github What The Hack.
…


New file 
run-e2e-tests.yml


name: Run cypress tests
on:
       pull_request: 
              branches: [“main”]

jobs: 
       runs-tests: 
             runs-on: ubuntu-latest
             steps: 

Github Actions Marketplace 
https://github.com/marketplace?type=actions
Search for apps and actions - checkout 
Actions  
Checkout 

Search for apps and actions - cypress
Actions
Cypress.io - https://github.com/marketplace/actions/cypress-io

End-End Testing 

name: End-to-end tests
on: push
jobs:
  cypress-run:
    runs-on: ubuntu-22.04
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      # Install npm dependencies, cache them correctly
      # and run all Cypress tests
      - name: Cypress run
        uses: cypress-io/github-action@v5

run-e2e-tests.yml


name: Run cypress tests
on:
       pull_request: 
              branches: [“main”]

jobs: 
       runs-tests: 
             runs-on: ubuntu-latest
             steps: 
           - name: Checkout
             uses: actions/checkout@v3
          # Install npm dependencies, cache them correctly
          # and run all Cypress tests
           - name: Cypress run
             uses: cypress-io/github-action@v5
             with: 
                   start: npm run start
                   build: npm run build
                   project: ./src
             env: 
                   MONGODB_URI: ${{ secrets.MONGODB_URI }}

Actions
Actions 
All workflow
Run Cypress tests

Settings
Secrets and variables - Actions
New repository secret 
Actions secrets / New secret
Name - MONGODB_URI
Secret - in memory
Add secret
Repository secrets
MONGODB_URI - edit 
Actions secret / update secret
MONGODB_URI
Value
…

Visual Studio Code 
Source Control
Message
… - branch ( create branch… )
New branch name - update-code 
Do you want to switch to the new branch?
Switch to Branch

src > pages > JS _app.js 
import ‘../css/styles.css’
import ‘../css/form.css’
import Head from ‘next/head’
import Link from ‘next/link’

function MyApp ({ Componet, pageProps }) {
       return ()
…
}

…

<h1>Wrong header</h1>

Visual Studio Code
Source Control 
Message - Updates header ( commit L ) 

Pull Request ( click on )
TITLE 
Updates header
Create

Pull Request #10
Updates header
#10
Open

Github 
Automating-Repetitive-Tasks-with-GitHub-Actions---AMER-EMEA/.github/workflows/
Actions
Actions
All workflow
Updates header - run-tests
Set up jobs
Checkout
Cypress run
Post Checkout

Cypress run
Cache size: ~150 MB ( 156838527 B )
…

Settings
Branches
Default branch
Branch protection rules - Add branch protection rule
Branch name pattern - main
Protect matching branches - Require a pull request before merging ( When enable, all commits must be made to a non-protected branch and submitted via a pull request before they can be merged into a branch that matches this rule ) 
Require status checks to pass before merging
Search for status checks in the last week for this repository - run tests ( Github Actions )
Create

Visual Studio Code 
CODEOWNERS 
# For more information, see [docs] (https://github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners#codeowners-syntax)

This repository is maintained by:
@geektrainer @peckjon

.github/workflows/* @geektrainer 

< 
Are you sure you want to discard changes in CODEOWNER ?
Discard Changes

CODEOWNERS 
# For more information, see [docs] (https://github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners#codeowners-syntax)

This repository is maintained by:
@geektrainer @peckjon

Github UI
Pull Requests
Update header
Run Cypress tests / run-tests (pull request)
Merging without waiting for requirements to be met (bypass branch protections)

Visual Studio Code
src > pages > JS _app.js 
import ‘../css/styles.css’
import ‘../css/form.css’
import Head from ‘next/head’
import Link from ‘next/link’

function MyApp ({ Componet, pageProps }) {
       return ()
…
}

…

<h1>Pets</h1>

Source Control 
Adds correct value 
Commit ( L ) 

Github UI
Pull Requests
Update header
Run Cypress tests / run-tests (pull request) - in progress 
Details 
run-tests
> Set up job
> Checkout 

Cypress run 
Post Checkout 
Complete job

Pull Requests
Update header
All checks have passed
This branch has no conflicts with the base branch 
Merge pull request

Start Templates
Guide your developers in finding the correct workflows 
Defaults provided by GitHub
Create your own for your organization 

Required workflows 
Configure a workflow that must run in repositories in an organization for all PR´s opened against the default branch
Allow you to implement organization-wide CI/CD policies that apply to current and future repositories 
Is triggered by PR events and appears as a requires status check
Blocks the ability to merge the PR until the required workflow succeeds 



