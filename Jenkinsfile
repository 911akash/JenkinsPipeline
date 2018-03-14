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
        sh "echo 'deploy the docker image'"
        sh "pip install docker-py"
        sh "ansible-playbook master.yaml"
        }
      }

    stage('on_master'){
      agent{
        docker {
          image 'akash/ansible:latest'
        }
      }
      when {
        branch 'master'
      }
    steps{
      sh "echo 'deploy the docker image'"
      sh "pip install docker-py"
      sh "ansible-playbook deploy.yml"
      }
    }

    }
  }
