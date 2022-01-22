# windows

<sub>[:arrow_upper_left: windows](../../readme.md) --- [**npm**](../../../../npm/nodejs/run.md) <sub> 

## execution-policy

```powershell
Get-ExecutionPolicy -List

Scope          ExecutionPolicy
-----          ---------------
MachinePolicy  Undefined
UserPolicy     Undefined
Process        Undefined
CurrentUser    AllSigned
LocalMachine   Undefined
```

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
```

<sub></sub>
----


[***referencia***](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/get-executionpolicy?view=powershell-7.2)

