pipeline {
  agent {
    label 'angular'
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
