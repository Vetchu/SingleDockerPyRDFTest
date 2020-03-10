node() {
    def pyrdf_docker
    stage ("Get image") {
        git 'http://localhost:3000/Vetch/DockerBaseTest.git'
    }
    stage("Build image"){
        pyrdf_docker = docker.build("dockerpyrdf","--network='host' .")
    }
    stage("Run image"){
        pyrdf_docker.inside{
            sh '. /root/bin/thisroot.sh && python2 PyRDF/introduction.py'
        }
    }
}