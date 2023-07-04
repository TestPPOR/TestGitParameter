pipeline {
  agent any
    parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'TAG', type: 'PT_TAG'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH_TAG', type: 'PT_BRANCH_TAG'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'REVISION', type: 'PT_REVISION'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'PULL_REQUEST', type: 'PT_PULL_REQUEST'
  }
  stages {
    stage('Delete workspace before build starts') {
        steps {
            echo 'Deleting workspace'
            deleteDir()
        }
      }
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", url: 'github.com/TestPPOR/TestGitParameter.git'
        git branch: "${params.TAG}", url: 'github.com/TestPPOR/TestGitParameter.git'
        git branch: "${params.BRANCH_TAG}", url: 'github.com/TestPPOR/TestGitParameter.git'
        git branch: "${params.REVISION}", url: 'github.com/TestPPOR/TestGitParameter.git'
        git branch: "${params.PULL_REQUEST}", url: 'github.com/TestPPOR/TestGitParameter.git'
      }
    }
    stage('Ls work dir') {
      steps {
          sh '''
              ls -la                  
          '''
      }
    }
  }
}