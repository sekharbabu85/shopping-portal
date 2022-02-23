pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the compile job'
        sh 'npm install'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the second job'
        sh 'npm test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the third job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Hey I know how to create pipeline as code...'
    }

  }
}