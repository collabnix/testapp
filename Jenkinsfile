pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/mhumair/testapp.git'

            // Run Maven on a Unix agent.
            

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

      }
      stage('Run') {
         steps{
            sh "node app"
         }
      }
    
   }
}
