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
	    tpJobRun agentId: '0OvZAzBaC0u4YUkqezrACg', jobId: 'GVHRxGQG40OQvCrFJvBuow', projectId: '6m1LeGuoB0qPgwS05Ew4yA', waitJobFinishSeconds: 3600
	    
	    sh "killall -9 node"

	 }
      }
   }
}
