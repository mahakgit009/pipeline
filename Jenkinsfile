pipeline{
    agent{
        label{
		    label 'built-in'
		}	
	}
	stages{
	    
		stage ('master'){
		        steps{
				    sh "sudo yum install httpd -y"
					sh "sudo service httpd start"
					sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
					
				}
		}
		stage ('node-1'){
            
			agent{
              
			    label{
		            
					label "172.31.36.181"
		        }	
	        }
			
			steps{
			      sh "sudo yum install httpd -y"
					sh "sudo service httpd start"
					sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
			}
    		
		}
		stage ('node-2'){
            
			agent{
              
			    label{
		             label "172.31.39.168"
		        }	
	        }
			steps{
			        sh "sudo yum install httpd -y"
				    sh "sudo service httpd start"
				 	sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
			}
    		
		}
	}
}
