pipeline {
    agent any
    stages {
        stage("Initialization") {
            steps {
                // use name of the patchset as the build name
                buildName "${BUILD_NUMBER}-${Release_Number}"
                buildDescription " Release Number ${Release_Number} was Executed on node ${NODE_NAME}"
            }
        }
        stage("Hello Stage") {
            steps {
                // use name of the patchset as the build name
              echo " This will pass test for Plugin";
            }
        }
    }
    post {
        success {
            buildDescription "Build passed with on Release Number ${Release_Number}"
        }
        failure {
            buildDescription "Build failed with on Release Number ${Release_Number}"
        }
    }
}
