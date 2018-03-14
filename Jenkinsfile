pipeline {
  agent any
  stages {
    stage('build_Image') {

    steps{
      sh "ansible-playbook master.yml"
      }
      }
    }
  }
