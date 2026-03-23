# Jenkins Pipelines

This repository contains a collection of Jenkins Declarative Pipelines designed to demonstrate CI/CD concepts using Docker agents.

## 🚀 Project Structure

my-first-pipeline : A basic pipeline that uses a single Docker agent (`node:16-alpine`) to verify environment configurations.
multi-stage-multi-agent : An advanced pipeline demonstrating how to use different Docker agents (Maven and Node.js) for separate build stages (Backend and Frontend).

## 🛠️ Prerequisites

To run these pipelines, you need:
Jenkins installed and running.
Docker Pipeline Plugin installed in Jenkins.
Docker nstalled on the Jenkins agent/host.

## 🏗️ How to Build

1. Create a New Item : In Jenkins, select "Pipeline".
2. Pipeline Definition : Choose "Pipeline script from SCM".
3. SCM : Select "Git" and paste your Repository URL.
4. Script Path : 
   * To run the first pipeline, set path to: `my-first-pipeline/Jenkinsfile`
   * To run the multi-stage pipeline, set path to: `multi-stage-multi-agent/Jenkinsfile`
5. Save & Build : Click "Build Now".

## 📊 Pipeline Logic
The multi-agent pipeline follows this workflow:
- Stage 1 (Back-end) : Uses `maven:3.8.1` to check Java environment.
- Stage 2 (Front-end) : Uses `node:16-alpine` to check JavaScript environment.
