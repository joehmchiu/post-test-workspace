pipeline {
  environment {
    bakdir = '~/backup/test-workspace'
  }

  agent any
  stages {
    stage('Pre Check') {
      steps {
        echo "testing..."
        sh "cd ${bakdir}/workspace"
        sh "cat .git/config"
      }
    }
    stage('Push Tag') {
      steps {
        echo "testing..."
        sh "cd ${bakdir}/workspace && git remote set-url origin git@github.com:/joehmchiu/test-workspace.git && git push --tag"
      }
    }
    stage('Post Check') {
      steps {
        echo "testing..."
        sh "cd ${bakdir}/workspace"
        sh "cat .git/config"
      }
    }
  }
}
