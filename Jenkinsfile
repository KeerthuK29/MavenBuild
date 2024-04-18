pipeline{
    agent any
    tools{
        maven "MAVEN_HOME"
    }
    stages{
        stage('Checkout'){
            steps{
                git "https://github.com/KeerthuK29/MavenBuild.git"
            }
        }
        stage('Compile code'){
            steps{
                bat "mvn compile"
            }
        }
        stage('Test'){
            steps{
                bat "mvn test"
            }
        }
        stage('Build'){
            steps{
                bat "mvn package"
                
            }
        }
    }
    post{
        failure{
            echo "Build failed"
        }
    }
}
