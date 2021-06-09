pipeline{
  
  agent any
  
  stages{
    
    stage("build"){
      
      steps{
        echo 'building the application...'
      } 
    }
    
    stage("test"){
      
      steps{
        echo 'testing the application...'
        echo jenkins ${NODE_NAME} ${JOB_NAME} ${EXECUTOR_NUMBER}
      } 
    }    
    
    stage("deploy"){
      
      steps{
        echo 'deploying the application...'
      } 
    }
  }
  
  post{
    
    always{
     echo jenkins-${NODE_NAME}-${JOB_NAME}-${EXECUTOR_NUMBER}
    }
    success{
      echo BUILD_NUMBER
    }
    
    failure{
      echo BUILD_NUMBER
    }
  }
}
