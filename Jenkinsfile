pipeline {
  agent none
  stages {
    stage('build_Image_on_Dev') {
      agent{
        docker {
          image 'akash/ansible:latest'
        }
      }
      when {
        branch 'dev'
      }
      steps{
        sh "ansible-playbook master.yaml"
        }
      }

    stage('on_master'){
      when {
        branch 'master'
      }
    steps{
      sh "echo 'deloy the docker image'"
      }
    }

    }
  }
