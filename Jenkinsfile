pipeline {
    agent any
    stages {
        stage('Get values') {
            input {
                message "please enter values"
                ok "Ok"
                submitter "no matter"
                parameters {
                    string(name: 'duration', defaultValue: '60', description: 'What is duration')
                    string(name: 'users', defaultValue: '5', description: 'How many users')
                    string(name: 'rampUp', defaultValue: '10', description: 'rampUp')
                }
            }
            steps {
                echo "duration, ${duration}, users, ${users}, rampUp, ${rampUp}."
            }
        }
        stage ('Run Load Test') {
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