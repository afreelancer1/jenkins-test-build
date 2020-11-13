pipeline {
    agent any
    stages{
        stage("build") {
            steps{
                sh '''./gradlew build clean'''
                echo "The build stage passed..."
            }
        }
    }post{
        always{
            echo "post-build will always run after build completed"
            // Jenkins cleans the workspace
            cleanWs()  
        }
    }
}
