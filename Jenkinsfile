node {
   stage 'Run Load Test'
   echo 'Starting test with Jmeter'
   bat """
    CALL CD C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin
    CALL RD /S /Q C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\BureacovaEntranceTask\\HTML
    CALL DEL "C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\BureacovaEntranceTask\\log.csv"
    CALL jmeter.bat -n -t C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\BureacovaEntranceTask\\TestPlanBureacovaUpdate.jmx ^
        -l C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\BureacovaEntranceTask\\log.csv -e -o C:\\Users\\EBureacova\\apache-jmeter-5.4.1\\bin\\BureacovaEntranceTask\\HTML ^
        -Jduration=%duration% -Jusers=%users% -jrampUp=%rampUp% -Jjmeterengine.force.system.exit=true
    """
   echo 'Test completed'
}