.PHONY: environment remove-env install uninstall test # .PHONY is something we can add when our target dependencies are not files.

MODULE=mcsim
ENVIRONMENT=chem274A_lab1

# by typing "make environment", we first go through the prerequisite and run `remove-env`, 
# which removes any environment with the name defined in (ENVIRONMENT), in this case `chem274A_lab1`;
# then it creates a new environment with python 3.9 package;
# then it installs all the libraries, including notebook, numpy, matplotlib in the environment;
environment: remove-env
	conda create -n $(ENVIRONMENT) "python=3.9" --yes
	conda install -c conda-forge notebook nbconvert numpy matplotlib pytest-cov pandas --name $(ENVIRONMENT) --yes

# we remove the environment `chem274A_lab1`;
remove-env:
	conda remove --name $(ENVIRONMENT) --all --yes

# we first go to prerequisite uninstall, then install all the packages
install: uninstall ## install the package to the active Python's site-packages
	pip install .

# we first go to prerequisite uninstall, then install all the packages and make them editable
dev-install: uninstall
	pip install -e .

uninstall: ## uninstall the package
	pip uninstall --yes $(MODULE)

# run pytest to validate the package functions
test: 
	pytest -v