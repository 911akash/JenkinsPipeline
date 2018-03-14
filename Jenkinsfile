pipeline {
  agent none
  stages {
    stage('build_Image') {
    agent {
      docker { image 'ansible/ansible:default' }
    }
    steps{
      sh "ansible-playbook master.yml"
      }
      }
    }
  }
