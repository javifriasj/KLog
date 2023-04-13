# KLog

KLog is a library which aims to bring easy logging in Python

<p align="center">
  <a href="https://github.com/javifriasj/KLog/releases/">
    <img alt="Releases" src="https://img.shields.io/github/v/release/javifriasj/KLog?label=release&logo=DocuSign&logoColor=%23fff&style=for-the-badge" />
  </a>
  
  <a href="https://pypi.org/project/KLogLib/">
    <img alt="PyPI" src="https://img.shields.io/github/v/release/javifriasj/KLog?label=pypi&logo=pypi&logoColor=%23fff&style=for-the-badge" />
  </a>
  
  <a href="https://github.com/javifriasj/KLog/blob/main/LICENSE">
    <img alt="Releases" src="https://img.shields.io/static/v1?label=Licence&message=MIT&style=for-the-badge&logoColor=%23fff" />
  </a>
</p>

<hr>

### Installation

```
pip install KLogLib
```

### Features

- Create Log folder/file
- Specify max log size (MB)
- Zip and save 'N' last log files

### Usage

First of all, we have to import the library

```
from KLog.KLog import KLog
```

Once we have imported it, we have to initialize the library

```
def init_log():
  logModel = KLog.__new__(KLog)

  logModel.__init__(folder='Logs/', log_name='log.log', max_size=50, is_zip=True, max_zip=10)
```

- folder: Path where the log file will be created.
- log_name: Name of the log file to be created.
- max_size: Maximum size of log files (MB)
- is_zip: Allow to create .zip files to save a backup of the log files.
- max_zip: Maximum .zip files.

The only thing left is to use the library

```
logModel.write(where='MainApplication', msg='Let`s logging', severity=KLog.LogSeverity.DEBUG)
```

- where: Method from where we are writing the log line.
- msg: Message that we want to be written in the log file.
- severity: Log line type, can be one of those:
  - <img alt="Warning" src="https://img.shields.io/badge/WARNING-yellow"/>
  - <img alt="Warning" src="https://img.shields.io/badge/DEBUG-green"/>
  - <img alt="Warning" src="https://img.shields.io/badge/ERROR-red"/>
  - <img alt="Warning" src="https://img.shields.io/badge/CRITICAL-red"/>
  - <img alt="Warning" src="https://img.shields.io/badge/INFO-blue"/>

<hr>

Example of deleting zips



https://user-images.githubusercontent.com/17411934/231798446-a4187172-878c-423a-9abd-1cf40e6c58bb.mov


