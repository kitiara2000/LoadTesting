pipeline {
    agent any
    stages {
        stage ('Run Load Test') {
			input {
                message "please enter values"
                ok "Ok"
                submitter "no matter"
                parameters {
                    string(name: 'duration', defaultValue: '60')
                    string(name: 'users', defaultValue: '5')
                    string(name: 'rampUp', defaultValue: '10')
                }
            }
            steps {
                echo 'Starting test with Jmeter'
                bat """
                 CALL C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\jmeter.bat -n -t TestPlanBureacovaUpdate.jmx ^
                    -Jduration=${duration} -Jusers=${users} -jrampUp=${rampUp} -Jjmeterengine.force.system.exit=true
                """
                echo 'Test completed'
            }
        }
    }
}