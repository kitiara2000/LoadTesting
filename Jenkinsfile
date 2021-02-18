node {
   stage ('Run Load Test') {
   echo 'Starting test with Taurus'
   bzt "jmeter/TestPlanBureacovaUpdate.jmx -report -o settings.artifacts-dir=artifacts"
   echo 'Test completed'
   }
}