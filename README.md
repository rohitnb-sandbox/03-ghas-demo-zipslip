# Code Scanning JavaScript Tutorial

Welcome to the Code Scanning JavaScript Tutorial! This tutorial will take you through how to set up GitHub Advanced Security: Code Scanning as well as interpret results that it may find. The following repository contains vulnerability [CVE-2018-20835](https://github.com/advisories/GHSA-x2mc-8fgj-3wmr) (aka Zip Slip).

## Introduction

Code scanning is a feature that you use to analyze the code in a GitHub repository to find security vulnerabilities and coding errors. Any problems identified by the analysis are shown in GitHub.

You can use code scanning with CodeQL, a semantic code analysis engine. CodeQL treats code as data, allowing you to find potential vulnerabilities in your code with greater confidence than traditional static analyzers.

This tutorial with use CodeQL Analysis with Code Scanning in order to search for vulnerabilities within your code. 

## Instructions

- [ ] Duplicate this repository using the "Use this Template" option
- [ ] Create a branch
- [ ] Modify L264 in `index.js` to `var srcpath = path.resolve(cwd, header.linkname)`
- [ ] Create a Pull Request
- [ ] Let the CodeQL Scanning complete
- [ ] Observe the generated alerts
- [ ] Change L264 `index.js` back to `var srcpath = path.join(cwd, path.join('/', header.linkname))`
- [ ] This should rerun CodeQL workflow and automatically fix the Open Alert
- [ ] Close the PR
