pipeline {
    agent any

    stages {
        stage('Greeting') {
            steps {
                echo 'Hello EMC Students, welcome to the world of CI/CD'
            }
        }

        stage('System Info') {
            steps {
                bat 'date /t'
                bat 'time /t'
                bat 'wmic logicaldisk get size,freespace,caption'
            }
        }

        stage('Build Simulation') {
            steps {
                echo 'Simulating build process...'
                bat 'echo Compiling... Testing... Packaging...'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL: Jenkins Pipeline CI/CD demo completed successfully!'
        }
        failure {
            echo 'BUILD FAILED: Please check the console output for errors.'
        }
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
