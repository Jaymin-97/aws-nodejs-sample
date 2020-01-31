pipeline{
	agent {
        node{
            label 'test'
        }
    }
	stages{
		stage('old backup delete'){
			steps{
				sh '''
				 rm -rf /home/ec2-user/backup/*
				'''
			}
		}
		stage('copy old file '){
			steps{
				sh'''
					cp -r ~/try  ~/backup
				'''
				}
	    }
	    stage('ccureent code delete'){
	    	step{
	    		sh'''
	    			rm -rf /home/ec2-user/try/*
	    		'''
	    	}
	    }
    stage('newcodecopy'){
    	steps{
    		sh '''
    		cp -r /home/ec2-user/workspace/pipeline /home/ec2-user/try
    		'''
    	}
    stage('build'){
    	steps{
    		sh '''
    		cd /home/ec2-user/try
    		npm i
    		'''
    	}
    }
stage('check'){
	steps{
		sh'''
		echo done
		'''
	}
    }		
}
}
