pipeline {
  agent any
    /*parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'develop', name: 'BRANCH', type: 'PT_BRANCH'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'develop', name: 'TAG', type: 'PT_TAG'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'develop', name: 'BRANCH_TAG', type: 'PT_BRANCH_TAG'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'develop', name: 'REVISION', type: 'PT_REVISION'
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'develop', name: 'PULL_REQUEST', type: 'PT_PULL_REQUEST'
  }*/
  stages {
    stage('Delete workspace before build starts') {
        steps {
            echo 'Deleting workspace'
            deleteDir()
        }
      }
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", credentialsId: 'ASadkov', url: 'https://git.sfera.org/PPOR/backend.git'
        git branch: "${params.TAG}", credentialsId: 'ASadkov', url: 'https://git.sfera.org/PPOR/backend.git'
        git branch: "${params.BRANCH_TAG}", credentialsId: 'ASadkov', url: 'https://git.sfera.org/PPOR/backend.git'
        git branch: "${params.REVISION}", credentialsId: 'ASadkov', url: 'https://git.sfera.org/PPOR/backend.git'
        git branch: "${params.PULL_REQUEST}", credentialsId: 'ASadkov', url: 'https://git.sfera.org/PPOR/backend.git'
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