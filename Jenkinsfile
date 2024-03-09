pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES1UG21CS696-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployment successful'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
      
