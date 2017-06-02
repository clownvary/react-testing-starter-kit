pipeline {
  agent any
  stages {
    stage('Print') {
      steps {
        echo 'Starting'
        acceptGitLabMR(mergeCommitMessage: 'This is test timestamp MergeCommitMessage')
      }
    }
    stage('CheckOut') {
      steps {
        git(url: 'git@github.com:clownvary/react-testing-starter-kit.git', branch: 'master', changelog: true)
      }
    }
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        sh 'npm run test'
      }
    }
  }
}