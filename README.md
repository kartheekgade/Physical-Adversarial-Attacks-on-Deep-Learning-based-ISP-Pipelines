# Physical-Adversarial-Attacks-on-Deep-Learning-based-ISP-Pipelines

## These are the steps to get PyNET-CA environment set up and running
1. Create new conda environment
	$ conda create -n pynet python=3.6
2. Activate the new environment
	$ conda activate pynet
3. Install dependencies
	$ conda install pytorch
	$ pip install torchvision
	$ pip install pytorch-mssim
	$ pip install IQA-pytorch
	$ pip install tqdm
4. Cd into repo directory 
	$ cd /skyb-aim2020-public/
5. Make changes to code
	- I am running this without GPU so in main.py we made the following changes
		device = ‘cpu’
		for the two “model.load_state_dict(torch.load()) we added the map_location
			the full line is now: model.load_state_dict(torch.load(os.path.join(args.target_dir, ‘model’, ‘/pretrained_model/result/pynetca/model/model_early_perceptual.pth’ if args.perceptual else ‘model_early_fidelity.pth’), map_location=torch.device(‘cpu’)))

6. Run the script
	$ python mian.py —skip_train —test_dir /Desktop/Adversarial_ISP/skyb-aim2020-public/data/test/huwaei_raw


6, 28, 41, 42, 43, 60, 81, 114, 115, 116, 117, 142, 158, 178, 179, 183, 184, 192, 201, 211, 212, 213, 222, 249,
250, 253, 302, 347, 348, 453, 466, 477, 481, 483, 500, 570, 583, 584, 609, 665, 666, 695, 714, 718, 719, 760, 784, 1013, 1046, 1051, 1052, 1064, 1065, 1114, 1115, 1124, 1174, 1189


