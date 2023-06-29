pipeline {
  agent {
    label 'angular'
  }
  stages {
    stage('install') {
      steps{
        echo'install'
      }
    }

    stage('build') {
      steps{
        echo'build'
      }
    }

    stage('deploy') {
      steps {
        sh "terraform apply --var-file='config/${params.tfenv}.tfvars' --auto-approve"
      }
    }
  }
}
