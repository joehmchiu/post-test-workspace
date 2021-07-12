pipeline {
  environment {
    bakdir = '~/backup/test-workspace'
  }

  agent any
  stages {
    stage('Push Tag') {
      steps {
        echo "testing..."
        sh "cd ${bakdir}/workspace"
        sh "git remote set-url origin git@github.com:/joehmchiu/test-workspace.git"
        sh "git push --tag"
      }
    }
  }
}
