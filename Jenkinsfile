pipeline {
    agent any
    stages {
        stage ('Run Load Test using Taurus') {
            steps {
                echo 'Starting test with Taurus'
                bat 'bzt taurus_jmeter_Myscript.yml                \
                        -o execution.0.ramp-up=float($rampUp)      \
                        -o execution.0.concurrency=float($users)   \
                        -o execution.0.hold-for=float($duration)   \
                        -report'
                echo 'Test completed'
            }
        }
    }
}
