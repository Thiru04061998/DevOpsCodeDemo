
pipeline{
    tools{
       
        maven 'Maven_3.9.11'
    }
	agent any
      stages{
           stage('Checkout the code'){
	    
               steps{
		 echo 'cloning the repo'
                 git 'https://github.com/Thiru04061998/DevOpsCodeDemo.git'
              }
          }
          stage('Compile'){
             
              steps{
                  echo 'complie the code again..'
                  bat 'mvn compile'
	      }
          }
          stage('CodeReview'){
		  
              steps{
		    
		  echo 'codeReview'
                  bat 'mvn pmd:pmd'
              }
          }
           stage('UnitTest'){
		  
              steps{
	         
                  bat 'mvn test'
              }
          
          }
        
          stage('Package'){
		  
              steps{
		  
                  bat 'mvn package'
              }
          }
	     
          
      }
}
