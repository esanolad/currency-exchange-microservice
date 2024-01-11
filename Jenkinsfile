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
}