pipelne {
    
    agent any
    
    stages{
        stages("Clone the project"){
            
            steps{
                
           git branch: 'main', url: 'https://github.com/pavanibantu/spring-petclinic.git'
                }
           }
 
           
           stage ("Build"){
               
               steps{
                   bat "mvn clean install"
               }
           }
                   
                stage ("Test"){
               
               steps{
                   bat "mvn test"   
               }
           }
            stage ("Generate the Junit test results"){
               
               steps{
                  junit 'target/surefire-reports/*.xml'
               }
            }
          stage ("Generate Artifact"){
               
               steps{
                 archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            
     }
 }
   