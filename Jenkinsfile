pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository
            git 'https://github.com/mhumair/testapp.git'

           
         }

      }
      stage('Run') {
	 steps {

	    sh "node app"

	 }
      }
//      stage('Cleanup') {
//	steps {
	  // sh killall -9 node	
//	}
  //    }
   }
}
