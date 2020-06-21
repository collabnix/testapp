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

	    sh "node index.js &"

	 }
      }
      stage('Test') {
	 steps {
	    tpJobRun agentId: 'ZEBz4h3YZUOxb5s8xTgVeg', jobId: 'EYQJ3tmcNkKqHhBOJ14P7w', projectId: 'ZUcm4zmEq0GrLCFEa2UgtQ', waitJobFinishSeconds: 3600
	    
	    sh "killall -9 node"

	 }
      }
   }
}
