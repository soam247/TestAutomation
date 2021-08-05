#!/usr/bin/env groovy
@Library(['piper-lib-os']) _

//Setup the skeleton for Jenkins based Runs
node {
    stage('System Tests') {
        deleteDir()

        // Clone code from the system test repository
        git '<YOUR GITHUB REPOSITORY>'

        // checkout the master branch
        sh 'git checkout master'

        // With this next step UIVeri5 tests can be executed.
        uiVeri5ExecuteTests script: this

        // HTML Publisher plugin
        // Publish HTML reports
        // Publish Test Report for UIveri5 on Jenkins  
        publishHTML target: [
            allowMissing: true,
            alwaysLinkToLastBuild: true,
            keepAll: true,
            reportDir: 'target/report/screenshots/',
            reportFiles: "report.html",
            reportName: "UIVeri5 Test Report"
        ]
    }
}
