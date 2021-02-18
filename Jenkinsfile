node {
   stage ('Run Load Test') {
   echo 'Starting test with Taurus'
   bat 'bzt **/TestPlanBureacovaUpdate/*.jmx -report' 
   echo 'Test completed'
   }
}