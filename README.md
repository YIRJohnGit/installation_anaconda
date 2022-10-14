# Installation Anaconda #



### Download from Repository ###
```
cd ~/Downloads
#curl https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh --output anaconda.sh
curl https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh --output anaconda.sh
ls -l
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195766377-b6a1d82f-3fe4-467c-9697-f24dd0b669a7.png)

### Execute the anaconda.sh script file ###
```
#sha256sum anaconda.sh
bash anaconda.sh
```
_Result_
![image](https://user-images.githubusercontent.com/111234771/195766582-72e9bc45-fde3-4d3c-9451-52ca99d9769b.png)

source ~/.bashrc

	conda list
	conda create --name my_env python=3
	conda activate my_env
	python --version
	conda deactivate

	conda create -n my_env35 python=3.5
	conda info --envs
	conda install --name my_env35 numpy
	conda create --name my_env python=3 numpy
	conda remove --name my_env35 --all

	conda update conda
	conda update anaconda

	conda install anaconda-clean
	anaconda-clean
	rm -rf ~/anaconda3

	nano ~/.bashrc



	# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/home/sammy/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/home/sammy/anaconda3/etc/profile.d/conda.sh" ]; then
        . "/home/sammy/anaconda3/etc/profile.d/conda.sh"
    else
        export PATH="/home/sammy/anaconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<

