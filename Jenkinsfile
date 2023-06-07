pipeline{
    agent any
    stages{
        stage("CLone the code"){
            steps{
                git url: 'https://github.com/doddamanisandeep/django-todo-cicd.git', branch:'develop'
                echo "code cloned"
            }
        }
        
        stage("Build") {
            steps{
                
               sh  "docker build -t django-todo-cicd ."
            }
        }
        
        stage("Create container") {
            steps{
            sh "docker run -d -p 8000:8000 django-todo-cicd"
            echo "container created"
            }
        }
        
        
    }
    
    
}
