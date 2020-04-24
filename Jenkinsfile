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
      stage('Test') {
	 steps {
runtpjob jobId: 'o7wS4nJc6Em3PEz_yqZErw', projectId: 'DzkGyzxkM0GLy799JBllVQ', waitJobFinishSeconds: 1800
	    sh "killall -9 node"

	 }
      }
   }
}
