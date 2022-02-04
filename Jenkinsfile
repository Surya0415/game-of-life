pipeline{
    agent {label 'master'}
    stages{
        stage('userdetails'){
            steps{
                sh 'whoami'
            }
        }
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Surya0415/game-of-life.git']]])
            }
        }
        stage('echo lastest commit'){
            steps{
                sh 'git log -1'
            }
        }
        stage('tar'){
            steps{
                sh 'tar -cvf myproject.tar .'
            }
        }
        
    }
}