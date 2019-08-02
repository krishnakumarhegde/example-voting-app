pipeline{
    
    agent any
    
    tools{
	maven 'Maven 3.6.1' 
    }

    stages {

        stage('build'){
            steps{
                echo 'Building worker app'
            	dir('worker'){
		sh 'mvn compile'
		}
	    }
        }
        stage(two){
            steps{
                echo 'hello world from step 2'
            }
        }
        stage(three){
            steps{
                echo 'hello world from step 3'
                sleep(5)
            }
        }
    }

    post{
        always{
            echo 'completed'
            sleep(6)
        }
    }
}
