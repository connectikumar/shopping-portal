pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test-the-job') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this shopping cart pipeline has completed...'
    }

  }
}