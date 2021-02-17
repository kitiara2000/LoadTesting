node {
   stage 'Run Load Test'
   echo 'Starting test with Jmeter'
   bat """
    CALL RD /S /Q HTML
    CALL DEL "log.csv"
    CALL C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\jmeter.bat -n -t TestPlanBureacovaUpdate.jmx ^
        -l log.csv -e -o HTML ^
        -Jduration=%duration% -Jusers=%users% -jrampUp=%rampUp% -Jjmeterengine.force.system.exit=true
    """
   echo 'Test completed'
}