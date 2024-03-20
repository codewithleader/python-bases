# Python - Bases

@codewithleader

# Python Version Manager

`pyenv --version`

`pyenv install --list`: List the versions available for download

`pyenv install 3.10.5`: Install python

`pyenv global 3.10.5`: Set global version

`pyenv local 3.10.5`: Create file `.python-version` with local version

# Virtual Enviroment

`python -m venv my_virtual_enviroment`: Create a virtual enviroment

- On Windows:

```powershell
my_virtual_enviroment\Scripts\activate
# Activate V. Enviroment
```

- On macOS or Linux/Git Bash:

```bash
source my_virtual_enviroment/bin/activate
# Or
source my_virtual_enviroment/Scripts/activate
# Activate V. Enviroment
```

- Instalar paquetes en el entorno virtual: Ahora que tu entorno virtual está activo, cualquier paquete que instales usando pip se instalará únicamente dentro de este entorno. Por ejemplo, para instalar face-recognition, simplemente ejecuta:

`pip install face-recognition`: Este paquete ahora estará disponible solo en el entorno virtual y no afectará a otros proyectos o al sistema global.

Puedes saber si un entorno virtual está activo en tu terminal por el cambio en el prompt. Cuando activas un entorno virtual, su nombre generalmente aparece entre paréntesis al principio de la línea del prompt. Por ejemplo, si tu entorno virtual se llama my_virtual_enviroment, verás algo como esto en tu terminal:

```bash
(my_virtual_enviroment) usuario@equipo:~/python-bases$ >
```

- Verificar la activación si no cambia el Prompt

```bash
which python
```

La salida que proporcionas indica que el intérprete de Python activo proviene de tu entorno virtual my_virtual_enviroment. La ruta /c/dev/Python/python-bases/\dev\Python\python-bases\my_virtual_enviroment/Scripts/python muestra que el comando python ahora apunta al intérprete dentro de la carpeta Scripts de tu entorno virtual, lo cual es lo esperado cuando el entorno está activo.

Aunque el prompt no cambie para mostrar el nombre del entorno (algo que puede variar dependiendo de la configuración de la terminal o shell que estés usando), la ruta del intérprete confirma que cualquier comando Python que ejecutes ahora usará el entorno virtual.

Ahora, al instalar paquetes usando pip, se instalarán en este entorno virtual y no afectarán la instalación global de Python. De igual manera, al ejecutar scripts de Python, se utilizará este entorno aislado. Así que, aunque no veas el nombre del entorno en el prompt, estás trabajando dentro del entorno virtual.

- Desactivar el entorno virtual: Cuando termines de trabajar en tu proyecto, puedes desactivar el entorno virtual ejecutando:

`deactivate`

- Usando entornos virtuales, puedes gestionar las dependencias de tus proyectos de manera aislada, evitando conflictos entre paquetes y asegurando que tu proyecto sea fácil de configurar en otras máquinas o entornos.

# Observaciones:

El comando python -m venv mi_entorno_virtual crea un entorno virtual en Python, que, en efecto, es similar a la carpeta node_modules en un proyecto Node.js, pero con una diferencia clave en la estructura y el propósito.

Cuando ejecutas este comando, se crea una carpeta llamada mi_entorno_virtual en tu directorio actual. Esta carpeta contiene una copia independiente del intérprete de Python, la biblioteca estándar y varios archivos de soporte, además de un espacio aislado para instalar bibliotecas adicionales.

La estructura general se ve así:

```bash
python-bases/
│
└───mi_entorno_virtual/  # El entorno virtual
│   │
│   ├───Include/
│   ├───Lib/
│   ├───Scripts/  # O 'bin' en Unix/Mac
│   └───...
│
└───tu_script.py  # Tus scripts de Python deben estar aquí, fuera de mi_entorno_virtual
```

No debes crear tus archivos .py dentro de mi_entorno_virtual. Esta carpeta es solo para el entorno virtual y sus bibliotecas. Tus scripts de Python (tu_script.py en el diagrama) deben residir fuera de esta carpeta, en la raíz de tu proyecto o en otra estructura de carpetas según tu organización.

mi_entorno_virtual no es la raíz de tu proyecto. Es solo una parte del proyecto, específicamente la que se encarga de mantener tu entorno aislado. La raíz de tu proyecto sigue siendo python-bases en tu ejemplo.

Activar el entorno virtual antes de trabajar. Antes de ejecutar o desarrollar tus scripts de Python, debes activar el entorno virtual. Esto asegura que cuando ejecutes Python o instales paquetes nuevos con pip, estás utilizando las versiones específicas dentro de tu entorno virtual y no las versiones globales instaladas en tu sistema.

Compartir tu proyecto sin el entorno virtual. Cuando compartes tu proyecto, generalmente no incluyes la carpeta del entorno virtual (mi_entorno_virtual). En cambio, puedes compartir un archivo requirements.txt con las dependencias, y cada usuario puede crear su propio entorno virtual en su sistema.

# Instalar librerias en el proyecto local

`pip install face_recognition`
