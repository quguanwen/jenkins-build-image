pipeline{
    agent{
        node{
          label "gradle"  //指定对应标签的构建节点
        }
    }
    options{
         buildDiscarder(logRotator(numToKeepStr: '20'))
 	}

 	stages{

 	    stage("clone"){
 	        steps{
 	            git 'https://github.com/quguanwen/my-demo-k8s.git'
 	        }
 	    }

        stage("build"){
            steps{
                script{
                    container("gradle"){
                        sh "gradle -v"
                    }
                }
            }
        }
        
        stage("docker-build"){
            steps{
                script{
                    sh "docker info"
                }
            }
        }
        
        stage("deploy"){
            steps{
                script{
                    sh "kubectl get node"
                }
            }
        }
 	}
}
