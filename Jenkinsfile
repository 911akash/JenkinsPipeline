pipeline {
  agent any
  stages {
    stage('build_Image_on_Dev') {
      when {
        branch 'dev'
      }
    steps{
      sh "echo 'created the docker image'"
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
