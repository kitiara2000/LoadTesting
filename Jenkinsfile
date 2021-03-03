pipeline {
    agent any
    stages {
        stage ('Run Load Test using Taurus') {
            steps {
                echo 'Starting test with Taurus'
                echo "duration, ${duration}, users, ${users}, rampUp, ${rampUp}."
                bat 'bzt taurus_jmeter_Myscript.yml         \
                      -o execution.0.ramp-up=%rampUp%      \
                      -o execution.0.concurrency=%users%   \
                      -o execution.0.hold-for=%duration%   \
                      //-o execution.0.scenario.modifications.enable=%Scenario% \
                      //-o modules.blazemeter.token=7d76b8b62734f8875d18f4ad:22d1e138688cb8fdcd41824f3cbb12f5f3c0a780924246313147989405a50cba924ea802  \ //valid till 31/03/21
                      -report'
                echo 'Test completed'
            }
        }
    }
}
