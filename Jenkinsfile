pipeline {
   agent any
   stages {
       stage('Run Load Test') {
           steps {
               script {
				echo 'Starting test with Jmeter'
				bat """
					CALL C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\jmeter.bat -n -t TestPlanBureacovaUpdate.jmx ^
					-Jjmeterengine.force.system.exit=true
				"""
				echo 'Test completed'
               }
           }
       }
   }
}