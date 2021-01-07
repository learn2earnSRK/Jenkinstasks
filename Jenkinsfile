pipeline{
    agent{
        label "CI" 
    }
	
parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    environment {
        APP_VERSION = '1.0'
	    SSH = credentials('ci-agent	')
    }

    stages{
        stage("stage-1"){
	environment{
		APP_VERSION = '2.0'
			}
            steps{
                sh 'env'
	    	}
	}
		stage('stage-II-mvn version'){
			steps{
				sh 'mvn --version'
   				     }
 				   }
	}
    }

