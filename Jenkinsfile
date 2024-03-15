pipeline{
  agent any
  stages{
    stage('Checkout'){
      steps{
        checkout scm
      }
    }
    stage('Build'){
      steps{
        sh '/home/onkar/Documents/Devops_Softawre/apache-maven-3.9.6/bin/mvn install'
      }
    }
    stage('Deployement'){
      steps{
        script{
          if (env.BRANCH_NAME == 'master') 
            {
            echo 'Hello from main branch'
            }
          if (env.BRANCH_NAME == 'null') 
            {
            echo 'Hello from null branch'
            }
          else {
            sh "echo 'Hello from ${env.BRANCH_NAME} branch!'"
            }
        }
      }
    }
  }
}
