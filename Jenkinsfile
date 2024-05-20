pipeline{
    agent {
        docker {image  "maven 3.3.3"}
    }
    
    stages{
        stage('Checkout'){
            steps{
                git branch :'master', url:"https://github.com/KeerthuK29/MavenBuild.git"
            }
        }
        stage('Compile code'){
            steps{
                sh "mvn compile"
            }
        }
        stage('Test'){
            steps{
                sh "mvn test"
            }
        }
        stage('Build'){
            steps{
                sh "mvn package"
                
            }
        }
    }
    post{
        failure{
            echo "Build failed"
        }
    }
}
