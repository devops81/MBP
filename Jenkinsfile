pipeline {
    agent any
    
    stages {
        stage ('Compile Stage') {
        def mvnHome = tool name: 'MVN3', type: 'maven'
            steps {
      
                    sh '${mvnHome}/bin/mvn clean compile'
         
                  }
                                }
        def mvnHome = tool name: 'MVN3', type: 'maven'
        stage ('Testing Stage') {

            steps  {
               
                    sh '${mvnHome}/bin/mvn test'
                
                   }
        }


        stage ('Deployment Stage') {
            steps {
                    def mvnHome = tool name: 'MVN3', type: 'maven'
                    sh '${mvnHome}/bin/mvn deploy'
                  }
        }
    }
}
