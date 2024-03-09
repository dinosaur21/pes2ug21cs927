pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    build 'pes2ug21cs927-1'
                    sh 'g++ -o output_file h1ello.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using a shell script
                    sh './output_file'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    // Perform deployment tasks, if any
                  echo 'deploy'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
