node {
    // Checkout the code from GitHub
    git branch: 'main', url: 'https://github.com/Shrouk-talaat/simple-java-app.git'

    stage('build') {
        try {
            sh 'echo "build stage"'
        } catch (Exception e) {
            sh 'echo "exception found"'
            throw e // Important to re-throw to fail the build properly
        }
    }

    stage('test') {
        if (env.BRANCH_NAME == "feat") {
            sh 'echo "test stage"'
        } else {
            sh 'echo "skip test stage"'
        }
    }
}