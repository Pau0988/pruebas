pipeline {
    //agent { docker { image 'ruby' } }
    agent any
    stages {
        stage('build') {
            steps {
                //add clone master branch
                git credentialsId: '981b4f45-b353-48b7-ac3f-ed64b1d86d42', url: 'https://github.com/Pau091288/rails-example-test'
            }
        }
        stage('develop') {
            steps {
                //add clone master branch
                echo 'prueba'
                //git credentialsId: '981b4f45-b353-48b7-ac3f-ed64b1d86d42', url: 'https://github.com/Pau091288/rails-example-test'
                //git (credentialsId: '981b4f45-b353-48b7-ac3f-ed64b1d86d42', url: 'https://github.com/Pau091288/rails-example-test', branch: 'develop')
            }
        }
        stage('staging')
        { 
            steps { 
                echo 'prueba1'
                //viewfeatures()
            }
        }
        stage('demo')
        { 
            steps { 
                echo 'prueba3'
            }
        }
        stage('production')
        { 
            steps { 
                echo 'prueba4'
            }
        }
        
    }
    
    
}

//Metodo para hacer descarga de las branches que sean feature

def viewfeatures ()
{ 
    git (credentialsId: '981b4f45-b353-48b7-ac3f-ed64b1d86d42', url: 'https://github.com/Pau091288/rails-example-test', branch: shortCommit)
    
    shortCommit = sh(returnStdout: true, script: "git branch | grep 'feature/*'").trim()
}
