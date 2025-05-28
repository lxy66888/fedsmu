We provide examples to demonstrate how FedSMU is implemented in the experiments. The datasets, model architecture and hyperparameters are described in detail in the paper. 

Notice that we put the dataset in the 'Folder'. For 100 clients and 10% participation rate, on the CIFAR-10 / CIFAR-100 dataset with Dirichlet (0.25) split and  Shakespreare dataset with non-iid data split, you can run code below. 

FedSMU:
python /code_fedsmu/main_fed.py --seed 200 --epochs 6000 --iid Dirichlet --rule_arg 0.25 --weigh_delay 0.001 --dataset CIFAR100 --model cnn --gpu 0 --num_users 100 --frac 0.1 --lr 0.01 --local_ep 5 --local_bs 50 --globallr1 0.018 --globallr2 0.01 --beta1 0.9 --beta2 0.9 --local_ep 5 --local_bs 50 --lr_decay 0.9988 --method fedsmu --filepath fedsmu_cifar100_num100_frac0.1__Dirichlet0.25.txt

python /code_fedsmu/main_fed.py --seed 200 --epochs 6000 --iid Dirichlet --rule_arg 0.25 --weigh_delay 0.001 --dataset CIFAR10 --model cnn --gpu 0 --num_users 100 --frac 0.1 --lr 0.1 --local_ep 5 --local_bs 50 --globallr1 0.015 --globallr2 0.01 --beta1 0.9 --beta2 0.9 --local_ep 5 --local_bs 50 --lr_decay 0.9988 --method fedsmu --filepath fedsmu_cifar10_num100_frac0.1_Dirichlet0.25.txt

python /code_fedsmu/main_fed.py --seed 200 --epochs 6000 --iid noniid --rule_arg 0.25 --weigh_delay 0.001 --dataset shakespeare --model rnn --gpu 0 --num_users 100 --frac 0.1 --lr 0.1 --local_ep 5 --local_bs 50 --globallr1 0.03 --globallr2 0.01 --beta1 0.95 --beta2 0.95 --local_ep 5 --local_bs 50 --lr_decay 0.999 --method fedsmu --filepath fedsmu_sh_num100_frac0.1_noniid.txt
