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
            sh '. /cern_root/root/bin/thisroot.sh && python2 /cern_root/root/PyRDF/introduction.py'
        }
    }
}