# Installation Anaconda #
## Tensorflow on Jupyter Notebook ##



### Download from Repository ###
```
cd ~/Downloads
curl  https://repo.anaconda.com/archive/Anaconda3-2023.07-2-Linux-x86_64.sh --output anaconda.sh

# curl -C https://repo.anaconda.com/archive/Anaconda3-2023.03-Linux-x86_64.sh --output anaconda.sh
#curl https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh --output anaconda.sh
#curl https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh --output anaconda.sh
ls -l
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195766377-b6a1d82f-3fe4-467c-9697-f24dd0b669a7.png)

### Execute the anaconda.sh script file ###
```
sha256sum anaconda.sh
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195768229-16116cba-cdba-4c17-bbd4-b7fe9b0f64f8.png)

```
bash anaconda.sh
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195766582-72e9bc45-fde3-4d3c-9451-52ca99d9769b.png)
![image](https://user-images.githubusercontent.com/111234771/195769695-a397a9cc-002b-4e8f-ab3e-8cc9c11d4fbe.png)
![image](https://user-images.githubusercontent.com/111234771/195769945-89b3bf51-eda3-44d9-933f-cfb041050e71.png)

- Syntax `eval "$(/home/<current user name>/anaconda3/bin/conda shell.bash hook)"`
Example:
```
eval "$(/home/$USER/anaconda3/bin/conda shell.bash hook)"
```
```
source ~/.bashrc
```
```
conda list
conda --version

conda update -n base -c defaults conda
```

### Creating Virtual Environment ###
```
conda create --name my_env python=3
conda activate my_env
python --version
```

### Close Virtual Environment ###
```
conda deactivate
```

```
conda create -n my_env35 python=3.5
conda info --envs
conda install --name my_env35 numpy
conda create --name my_env python=3 numpy
conda remove --name my_env35 --all

conda update conda
conda update anaconda
```

___Reboot the Machine (Optional)___
### Verify By Starting Jupyter Notebook ###
```
cd ~/anaconda3
jupyter notebook
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195773081-6d309d2c-e311-4f43-9424-460c4981179d.png)

### Start Anaconda Navigator and install Tensorflow ###
```
cd ~/anaconda3
anaconda-navigator
```
_Result: Setting Up for Tensorflow Environment_
![image](https://user-images.githubusercontent.com/111234771/195862893-6f5ec470-5070-49ae-9348-51164d48df9f.png)

_Running Sample Tensorflow_


### Removing Anacond3 ###
```
cd ~/anaconda3
eval "$(/home/$USER/anaconda3/bin/conda shell.bash hook)"

conda install anaconda-clean
anaconda-clean
rm -rf ~/anaconda3
nano ~/.bashrc

# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/home/$USER/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/home/$USER/anaconda3/etc/profile.d/conda.sh" ]; then
        . "/home/$USER/anaconda3/etc/profile.d/conda.sh"
    else
        export PATH="/home/$USER/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<
```
