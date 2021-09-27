# Connecting to TensorBoard from Remote Server

*  Launch Tensorboard on remote server: 
  
    ```
    tensorboard --logdir=path/to/log/dir --port=6000
    ```
  
    ***Note:** TRUBA raises error since Tensorboard tries to use 'tmp' dir. To handle this, run the following commands before launching Tensorboard:*
    
    ```
    export TMPDIR=/tmp/USER 
    mkdir $TMPDIR
    ```
    
*  Set up ssh port forwarding to an **unused** local ports on the local machine:

    ```
    ssh -NfL localhost:16006:localhost:6000 username@remoteip.   
    ```
* Go to localhost:16006 on the browser. 

**Reference:** [http://cerfacs.fr/helios/research_blog/tensorboard/](http://cerfacs.fr/helios/research_blog/tensorboard/)


