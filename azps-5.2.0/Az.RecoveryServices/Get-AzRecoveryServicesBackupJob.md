---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262053"
---
# Get-AzRecoveryServicesBackupJob

## Sinopse

Obtém trabalhos de backup.

## SYNTAX

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO

O cmdlet **Get-AzRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.
Defina o contexto do cofre usando o parâmetro-Cofreid.

## EXEMPLOS

### Exemplo 1: obter todos os trabalhos em andamento

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.
O segundo comando exibe o primeiro item na matriz de $Joblist.

### Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

Esse comando obtém trabalhos com falha da semana passada no cofre.
O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.
O comando não especifica um valor para o parâmetro *to* .
Portanto, ele usa o valor padrão do tempo atual.

### Exemplo 3: obter um trabalho em andamento e esperar a conclusão

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

Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.

Observação: você pode usar o cmdlet **Wait-AzRecoveryServicesBackupJob** para esperar que um trabalho de backup do Azure seja concluído em vez de While.

### Exemplo 4: obter todos os trabalhos do AzureVM nos últimos 2 dias que terminaram com êxito

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
O primeiro cmdlet busca o objeto do cofre. O segundo cmdlet armazena todos os trabalhos AzureVM no cofre especificado que foram concluídos nos últimos 2 dias para $jobs. Altere o valor do parâmetro BackupManagementType para MAB a fim de buscar trabalhos do agente do MAB.

## OS

### -BackupManagementType

A classe de recursos que estão sendo protegidos. Atualmente, os valores com suporte para esse cmdlet são AzureVM, AzureStorage, AzureWorkload, MAB.

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

As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.
Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .
Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .
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

Especifica o trabalho a obter.

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

Especifica a ID de um trabalho que o cmdlet obtém.
A ID é a propriedade JobId de um objeto **Microsoft. Azure. Commands. recoveryservices. backup. cmdlets. Models. JobBase** .

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
Os valores aceitáveis para esse parâmetro são:

- Fazer
- ConfigureBackup
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
Os valores aceitáveis para esse parâmetro são:

- InProgress
- Conseguiu
- Cela
- Cancelamento
- Feito
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

### -To

Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.
O valor padrão é a hora atual do sistema.
Se você especificar esse parâmetro, também deverá especificar o parâmetro **-from** .
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

### -Cofreid

ID do braço do cofre de serviços de recuperação.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase

## INFORMA

## LINKS RELACIONADOS

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Parar-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
