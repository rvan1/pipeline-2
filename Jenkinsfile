pipeline {
    agent any
    stages { 
        stage('Git clone') {
		    steps{
                // git url:'git@git.proj.git' ,  credentialsId: 'gitid'
                echo 'git clone'
            }
        }
        stage('sonar'){
		   steps {
		        echo 'install & run sonar preview'
			    // sh 'npm install sonarqube-scanner' 
			    // sh 'npm run sonarqube'
		   }
		}
        stage('install') {
            steps {
                echo 'npm install'
                sh 'node -v'		   
                // sh 'npm install'
              
            }
        }
        stage('lint'){
            steps {
                echo 'run lint'
                // sh 'npm install standard snazzy'
                // sh 'npm run lint'

            }
        }	
		stage('test'){
			steps{
			    echo ' testing.. '
			//	sh 'npm run build'
			//	sh 'npm test'
			}
		}	
		stage('cleanup'){
		 steps{
			echo 'prune and cleanup'
            // sh 'npm prune'
            // sh 'rm node_modules -rf'
		 }
		}
  
    }
	post {
	   success {
           	echo 'Success'
		    
        }
	}
}

