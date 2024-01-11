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
    agent any
    stages {
        stage('Build') {
            steps {
                echo(message: 'Build')
            }
        } post{
            always {echo(message: 'Build running')}
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
    } post{
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