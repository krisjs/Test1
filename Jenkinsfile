pipeline {
	agent any
	
	parameters { choice(name: 'CHOICES', choices: ['one', 'two', 'three'], description: '') }
	
	stages{
		stage ('Compile') {
			steps {
			    sh 'ls'
					
					echo 'findbuild scans'
					git credentialsId: '0ee5b254-2b1a-4442-9791-6bae35ec6bb7', url: 'https://github.com/krisjs/docker-spring-boot.git'
					sh 'ls'
					sh 'mvn clean compile'
				echo "Choice: ${params.CHOICE}"
				
			}
		
		}
		stage ('Testing') {
		steps {
				echo 'Tested'
			
			}
			
		}
		stage ('Deploy') {
		steps {	
					echo 'wow.. deployed'
			
			}
			
		}
	}
	
	post {
	    always{
	        
	        archiveArtifacts artifacts: 'Jenkinsfile', followSymlinks: false
	    }
	}
}
