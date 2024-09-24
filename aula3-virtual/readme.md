Ao fazer os imports:
import MetaTrader5 as mt5
import time

Tive o erro:
A module that was compiled using NumPy 1.x cannot be run in
NumPy 2.1.1 as it may crash. To support both 1.x and 2.x
versions of NumPy, modules must be compiled with NumPy 2.0.
Some module may need to rebuild instead e.g. with 'pybind11>=2.12'.

If you are a user of the module, the easiest solution will be to
downgrade to 'numpy<2' or try to upgrade the affected module.
We expect that some modules will need time to support NumPy 2.

Para resolver:
Criar ambiente virtual por causa do numpy 

conda create --name aula3-varos python=3.12.5

conda activate aula3-varos

pip uninstall numpy
pip install numpy<2.0

Exemplo:
#
# To activate this environment, use
#
#     $ conda activate virtconda (no venv .\virt\Scripts\Activate para ativar o ambiente de nome virt) (no linux usar o source na frente)
#
# To deactivate an active environment, use
#
#     $ conda deactivate (no venv basta deactivate)

listar os ambientes virtuais:
conda env list
ou
conda info --envs

Comando para ver o ambiente virtual ativo:
Pode usar o "conda env list" e ver onde está marcado com o asterisco indicando o ambiente ativo
ou
conda env list | grep '\*'

-----------------------
pip install notebook

jupyter notebook
