pipeline {
  agent {
    label 'jenkins-slave'
  }

  environment {
  }

  stages {
    stage('install') {
      echo'install'
    }

    stage('build') {
      echo'build'
    }

    stage('deploy') {
      steps {
        sh "terraform apply --var-file='config/${params.tfenv}.tfvars' --auto-approve"
      }
    }
  }
}
