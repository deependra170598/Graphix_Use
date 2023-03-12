#### The sudo prime-select query command is used to query the current GPU mode on Ubuntu. The output of "on-demand" means that your system is currently set to use the on-demand mode, which is a hybrid mode that allows the system to switch between the integrated GPU and the dedicated GPU (NVIDIA or AMD) based on the application's needs.
    sudo prime-select query
    
In on-demand mode, the integrated GPU is used by default, and the dedicated GPU is only activated when an application that requires it is launched. This can help to save power and reduce heat when the dedicated GPU is not needed.

#### You can switch between different GPU modes using the prime-select command. For example, you can switch to the NVIDIA GPU using the command sudo prime-select nvidia, or switch to the integrated GPU using the command sudo prime-select on-demand.
    sudo prime-select nvidia
    sudo prime-select on-demand

#### Switch to the AMD GPU: You can switch to the AMD GPU by using the DRI_PRIME environment variable. For example, to run the glxgears benchmark using the AMD GPU, you can run the following command in a terminal:
    DRI_PRIME=0 glxgears
This will run the glxgears benchmark using the integrated GPU.
    DRI_PRIME=1 glxgears
This will run the glxgears benchmark using the dedicated GPU.
   DRI_PRIME=<GPU_NUMBER> code 
This will run the vscode application using the mentioned GPU.
