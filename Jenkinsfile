pipeline {
    agent {
        docker {
            image 'hello-world' 
            args '-v /root/.m2:/root/.m2 -v /var/run/docker.sock:/var/run/docker.sock' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
