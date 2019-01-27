pipeline {
    agent any
    
    stages {
        stage ('Compile Stage') {
        def mvnHome = tool name: 'MVN3', type: 'maven'
            steps {
      
                    sh '${mvnHome}/bin/mvn clean compile'
         
                  }
                                }

        stage ('Testing Stage') {

            steps  {
               
                    sh '${mvnHome}/bin/mvn test'
                
                   }
        }


        stage ('Deployment Stage') {
            steps {

                    sh '${mvnHome}/bin/mvn deploy'
                  }
        }
    }
}
