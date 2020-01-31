pipeline{
	agent {
        node{
            label 'test'
        }
    }
	stages{
		stage('node install'){
			steps{
				sh '''
				npm i
				'''
			}
		}
		stage('check'){
		steps{
			sh'''
				echo hello
			'''
		}
		}
		
	}
}
