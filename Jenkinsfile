pipeline{
  
  agent any
  
  environment{
    SERVER_CREDENTIALS = credentials('fee11ee8-e14f-4982-ad78-8ba66a828838')
  }
  
  
  stages{
    
    stage("build"){
      
      steps{
        echo 'building the application...'
      } 
    }
    
    stage("test"){
      
      steps{
        echo 'testing the application...'
        echo "jenkins ${NODE_NAME} ${JOB_NAME} ${EXECUTOR_NUMBER}"
      } 
    }    
    
    stage("deploy"){
      
      steps{
        echo 'deploying the application...'
        echo "deploying with ${SERVER_CREDENTIALS}"
      } 
    }
  }
  
  post{
    
    always{
     echo "jenkins-${NODE_NAME}-${JOB_NAME}-${EXECUTOR_NUMBER}"
    }
    success{
      echo BUILD_NUMBER
    }
    
    failure{
      echo BUILD_NUMBER
    }
  }
}
