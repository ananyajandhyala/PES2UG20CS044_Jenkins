pipeline {
    agent any

stages{
  stage('Build') {
    steps{
      sh 'g++ -o PES2UG20CS044 PES2UG20CS044.cpp'
      build job: 'PES1UG20CS044-1'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS044'
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL'
    }
  }
}
post {
    failure {
        echo 'Pipeline Failed'
    }
  }
}

