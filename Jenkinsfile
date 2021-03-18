pipeline {
  agent any
  stages {
    stage('Code') {
      parallel {
        stage('Code') {
          steps {
            echo 'Code Commit'
          }
        }

        stage('Build') {
          steps {
            echo 'Building application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing Application'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: "Do you want to Deploy your Application ?", id: 'OK')
        echo 'Deploying Application'
      }
    }

  }
}
