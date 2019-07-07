pipeline{
    agent {label  'Yoni'}
    stages{
    stage('clone'){
            steps{
                git 'https://github.com/yoni12ab/sela-pipeline-demo.git'
            }
        }
     stage('install'){
            steps{
               sh 'npm install'
            }
        }
    stage('test'){
            steps{
              sh 'npm test'
            }
        }
    stage('build'){
            steps{
              sh 'npm run build'
            }
        }
    stage('Archive artifacts'){
            steps{
                archiveArtifacts '*.zip'
            }
        }
    }
}
