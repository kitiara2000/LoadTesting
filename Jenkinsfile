pipeline {
    agent any
    stages {
        stage ('Run Load Test with parameters') {
            steps {
                echo 'Starting test with Jmeter'
                bat """
                 CALL C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\jmeter.bat -n -t TestPlanBureacovaUpdate.jmx ^
                    -Jduration=%duration% -Jusers=%users% -jrampUp=%rampUp% -Jjmeterengine.force.system.exit=true
                """
                echo 'Test completed'
            }
        }
    }
}