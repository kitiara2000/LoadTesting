node {
   stage ('Run Load Test') {
   echo 'Starting test with Taurus'
   parallel (
	BlazeMeterTest: {
		dir ('Taurus-Repo') {
			sh 'bzt TestPlanBureacovaUpdate.jmx -report'
		}
	}
   ) 
   echo 'Test completed'
   }
}