pipeline {
   agent any
   stages {
       stage('read') {
           steps {
               script {
				echo 'Starting test with Taurus'
				bzt "jmeter/TestPlanBureacovaUpdate.jmx -report -o settings.artifacts-dir=artifacts"
				echo 'Test completed'
               }
           }
       }
   }
}