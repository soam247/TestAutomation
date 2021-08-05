#!/usr/bin/env groovy
@Library(['piper-lib-os']) _

//Setup the skeleton for Jenkins based Runs
node {
    stage('System Tests') {


        // With this next step UIVeri5 tests can be executed.
        uiVeri5ExecuteTests script: this

    }
}
