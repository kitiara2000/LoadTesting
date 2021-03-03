pipeline {
    agent any
    stages {
        stage ('Run Load Test') {
            steps {
                echo 'Starting test with Taurus'
                bat 'bzt taurus_jmeter_Myscript.yml -o execution.0.ramp-up=10 -o execution.0.concurrency=5 -o execution.0.hold-for=100 -report'
                echo 'Test completed'
            }
        }
    }
}
