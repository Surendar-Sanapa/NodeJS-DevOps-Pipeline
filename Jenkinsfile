pipeline { 
    environment { 
        registry = "surendarsanapa123/dockerimages" 
        registryCredential = 'docker-token' 
        dockerImage = ''
    }
    agent any 
    stages {
      stage('Building our image') {
        steps {
          script { 
            dockerImage = docker.build registry + ":$BUILD_NUMBER" 
          }
         }
       }
       stage('Deploy our image') { 
        steps { 
          script { 
            docker.withRegistry( '', registryCredential ) { 
              dockerImage.push()
            }
          } 
         }
        }   
     }
} 
