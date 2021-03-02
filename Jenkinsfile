pipeline {
    agent any
    stages {
        stage ('Run Load Test') {
            steps {
                echo 'Starting test with Taurus'
                sh 'bzt TestPlanBureacovaUpdate.jmx -o execution.0.ramp-up=$rampUp -o execution.0.concurrency=$users -o execution.0.hold-for=$duration -report'
                echo 'Test completed'
            }
        }
    }
}
