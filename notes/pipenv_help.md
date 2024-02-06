# `pipenv` Help

1. Check `pipenv` help to see the available commands and options:

`pipenv --help`

```powershell
PS C:\Users\FlynntKnapp\Programming\pipenv-basics> pipenv --help
Usage: pipenv [OPTIONS] COMMAND [ARGS]...

Options:
  --where                         Output project home information.
  --venv                          Output virtualenv information.
  --py                            Output Python interpreter information.
  --envs                          Output Environment Variable options.
  --rm                            Remove the virtualenv.
  --bare                          Minimal output.
  --man                           Display manpage.
  --support                       Output diagnostic information for use in
                                  GitHub issues.
  --site-packages / --no-site-packages
                                  Enable site-packages for the virtualenv.
                                  [env var: PIPENV_SITE_PACKAGES]
  --python TEXT                   Specify which version of Python virtualenv
                                  should use.
  --clear                         Clears caches (pipenv, pip).  [env var:
                                  PIPENV_CLEAR]
  -q, --quiet                     Quiet mode.
  -v, --verbose                   Verbose mode.
  --pypi-mirror TEXT              Specify a PyPI mirror.
  --version                       Show the version and exit.
  -h, --help                      Show this message and exit.


Usage Examples:
   Create a new project using Python 3.7, specifically:
   $ pipenv --python 3.7

   Remove project virtualenv (inferred from current directory):
   $ pipenv --rm

   Install all dependencies for a project (including dev):
   $ pipenv install --dev

   Create a lockfile containing pre-releases:
   $ pipenv lock --pre

   Show a graph of your installed dependencies:
   $ pipenv graph

   Check your installed dependencies for security vulnerabilities:
   $ pipenv check

   Install a local setup.py into your virtual environment/Pipfile:
   $ pipenv install -e .

   Use a lower-level pip command:
   $ pipenv run pip freeze

Commands:
  check         Checks for PyUp Safety security vulnerabilities and against
                PEP 508 markers provided in Pipfile.
  clean         Uninstalls all packages not specified in Pipfile.lock.
  graph         Displays currently-installed dependency graph information.
  install       Installs provided packages and adds them to Pipfile, or (if no
                packages are given), installs all packages from Pipfile.
  lock          Generates Pipfile.lock.
  open          View a given module in your editor.
  requirements  Generate a requirements.txt from Pipfile.lock.
  run           Spawns a command installed into the virtualenv.
  scripts       Lists scripts in current environment config.
  shell         Spawns a shell within the virtualenv.
  sync          Installs all packages specified in Pipfile.lock.
  uninstall     Uninstalls a provided package and removes it from Pipfile.
  update        Runs lock, then sync.
  upgrade       Resolves provided packages and adds them to Pipfile, or (if no
                packages are given), merges results to Pipfile.lock
  verify        Verify the hash in Pipfile.lock is up-to-date.
PS C:\Users\FlynntKnapp\Programming\pipenv-basics>
```

1. Explanation of `Usage: pipenv [OPTIONS] COMMAND [ARGS]...`

[Pipenv Command Syntax Explanation](https://chat.openai.com/share/85e4f104-70a1-4cff-bb1c-bac13e44e4bb)

The `pipenv --help` command provides information on how to use Pipenv, which is a tool for managing Python package dependencies. The specific part you're asking about explains the general syntax for using `pipenv` commands. Here's a breakdown:

- `Usage:`: This is a standard prefix in command-line documentation that introduces the syntax for using the command.

- `pipenv`: This is the name of the command-line tool you're using. When you type `pipenv` in your terminal or command prompt, you're invoking the Pipenv tool.

- `[OPTIONS]`: The square brackets indicate that providing options is optional. `OPTIONS` are flags or settings you can apply to modify the behavior of the `pipenv` command. These might include things like `--verbose` for more detailed output or `--python` to specify a particular version of Python for the environment. Since the options are in square brackets, it means you can choose to include none, one, or multiple options when you run a command.

- `COMMAND`: This is a placeholder for the specific Pipenv command you want to run. Pipenv supports several commands such as `install` to install packages, `uninstall` to remove them, `lock` to generate a `Pipfile.lock`, etc. This part of the syntax tells you that you must specify what action you want Pipenv to perform.

- `[ARGS]...`: Similar to `[OPTIONS]`, the square brackets indicate that arguments are optional. `ARGS` stands for the arguments that the specific `COMMAND` might require or accept. For example, if your command is `pipenv install`, `ARGS` could be the names of packages you want to install. The ellipsis (`...`) indicates that you can specify multiple arguments if needed.

Putting it all together, this syntax tells you that to use Pipenv, you start with the `pipenv` keyword, optionally include some global options, then specify the command you want to perform, and finally provide any arguments needed for that command. Here are a few examples to illustrate:

- To create a new virtual environment with a specific version of Python:
  ```
  pipenv --python 3.8
  ```
- To install a package:
  ```
  pipenv install requests
  ```
- To uninstall a package:
  ```
  pipenv uninstall requests
  ```
In each example, the parts of the command align with the `[OPTIONS] COMMAND [ARGS]...` structure described in the `pipenv --help` output.
