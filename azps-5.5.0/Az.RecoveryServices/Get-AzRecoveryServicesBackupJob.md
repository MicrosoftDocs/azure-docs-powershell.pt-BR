---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112697"
---
# Get-AzRecoveryServicesBackupJob

## Sinopse

Obtém trabalhos de backup.

## Sintaxe

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição

O cmdlet **Get-AzRecoveryServicesBackupJob obtém** trabalhos de Backup do Azure para um cofre específico.
De definir o contexto do cofre usando o parâmetro -VaultId.

## Exemplos

### Exemplo 1: Obter todos os trabalhos em andamento

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, o armazena na variável $Joblist dados.
O segundo comando exibe o primeiro item na matriz $Joblist dados.

### Exemplo 2: Obter todos os trabalhos com falha nos últimos 7 dias

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Esse comando recebe trabalhos com falha da última semana no cofre.
O *parâmetro De* especifica uma hora sete dias no passado especificada em UTC.
O comando não especifica um valor para o *parâmetro* Para.
Portanto, ele usa o valor padrão da hora atual.

### Exemplo 3: Obter um trabalho em andamento e aguardar a conclusão

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Este script vota no primeiro trabalho que está em andamento até que o trabalho seja concluído.

Observação: você pode usar o cmdlet **Wait-AzRecoveryServicesBackup Job** para aguardar a finalização de um trabalho de Backup do Azure em vez de Enquanto.

### Exemplo 4: Obter todos os trabalhos do AzureVM nos últimos 2 dias que foram concluídos com êxito

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
O primeiro cmdlet busca o objeto do cofre. O segundo cmdlet armazena todos os trabalhos do AzureVM no cofre determinado que foi concluído nos últimos 2 dias para $jobs. Altere o valor do parâmetro BackupManagementType para MAB para buscar trabalhos de agente MAB.

## Parâmetros

### -BackupManagementType

A classe de recursos que está sendo protegida. Atualmente, os valores com suporte para este cmdlet são AzureVM, AzureStorage, AzureWorkload, MAB.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile

As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -De

Especifica o início, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.
Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**
Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.
Use o formato UTC para datas.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho

Especifica o trabalho a ser feito.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Especifica a ID de um trabalho que este cmdlet obtém.
A ID é a propriedade JobId de um objeto **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operação

Especifica uma operação dos trabalhos que este cmdlet obtém.
Os valores aceitáveis para este parâmetro são:

- Backup
- ConfigurarBackup
- DeleteBackupData
- DisableBackup
- Restaurar
- BackupDataMove

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status

Especifica um status dos trabalhos que este cmdlet obtém.
Os valores aceitáveis para este parâmetro são:

- Inprogress
- Falhou
- Cancelado
- Cancelar
- Concluído
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Para

Especifica o fim, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.
O valor padrão é o tempo atual do sistema.
Se você especificar esse parâmetro, também deverá especificar o **parâmetro -From.**
Use o formato UTC para datas.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ID arm do Cofre de Serviços de Recuperação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## Notas

## LINKS RELACIONADOS

[Get-AzRecoveryServicesBackupServiceDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
