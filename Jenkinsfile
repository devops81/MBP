pipeline {
    agent any
    tools {
        maven 'Maven3'

    }
    stages {
        stage ('Compile Stage') {
        
            steps {
      
                    sh 'mvn clean compile'
         
                  }
                                }

        stage ('Testing Stage') {

            steps  {
               
                    sh 'mvn test'
                
                   }
        }


        stage ('Send out email Notification') {
            steps {
                emailext body: '$DEFAULT_CONTENT', subject: '$DEFAULT_SUBJECT', to: 'devops81@gmail.com'
                  }
    }
    }
}
