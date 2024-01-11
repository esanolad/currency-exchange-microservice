// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Testing integration"
// 	}
// }
pipeline {
    // agent any
    agent{
        docker {image 'maven:latest'}
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                echo(message: 'Build')
            }
        } 
        stage('Test') {
            steps {
                echo(message: 'testing')
            }
        }
        stage('Integrate') {
            steps {
                echo(message: 'Integrating')
            }
        }

    } 
    post {
        failure {
            echo(env.BUILD_ID)
        }
        success {
            echo(env.JENKINS_URL)
        }
        always {
            echo(message: 'I run always')
        }
        
    }
}