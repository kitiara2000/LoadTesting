node {
   stage 'Run Load Test'
   echo 'Starting test with Jmeter'
   bat """
    CALL CD %WORKSPACE%\\bin
    CALL RD /S /Q %WORKSPACE%\\bin\\BureacovaEntranceTask\\HTML
    CALL DEL "%WORKSPACE%\\bin\\BureacovaEntranceTask\\log.csv"
    CALL jmeter.bat -n -t %WORKSPACE%\\bin\\BureacovaEntranceTask\\TestPlanBureacovaUpdate.jmx ^
        -l %WORKSPACE%\\bin\\BureacovaEntranceTask\\log.csv -e -o %WORKSPACE%\\bin\\BureacovaEntranceTask\\HTML ^
        -Jduration=%duration% -Jusers=%users% -jrampUp=%rampUp% -Jjmeterengine.force.system.exit=true
    """
   echo 'Test completed'
}