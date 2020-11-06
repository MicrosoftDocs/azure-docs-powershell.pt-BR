---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599696"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## Sinopse
Esse comando lista os pontos de início e de término da cadeia de logs desfeitas do item de backup fornecido. Use-o para determinar se o point-in-time, ao qual o usuário deseja que o banco de usuários seja restaurado, é válido ou não.

## SYNTAX

### NoFilterParameterSet (padrão)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** Obtém os pontos de recuperação de intervalo de tempo no tempo para um item de backup do Azure com backup.
Após o backup de um item, um objeto **AzRecoveryServicesBackupRecoveryLogChain** tem um ou mais intervalos de tempo de recuperação.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

O primeiro comando obtém a data de sete dias atrás e, em seguida, armazena-o na variável $StartDate.
O segundo comando obtém a data de hoje e, em seguida, armazena-o na variável $EndDate.
O terceiro comando obtém contêineres de backup do AzureWorkload e os armazena na variável $Containers.
O quarto comando obtém o item de backup e, em seguida, armazena-o na variável $BackupItem.
O último comando obtém uma matriz de intervalos de tempo de ponto de recuperação para o item em $BackupItem e, em seguida, armazena-os na variável $RP.

## OS

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

### -EndDate
Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Objeto de item protegido para o qual o ponto de recuperação precisa ser buscado

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StartDate
Hora de início do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase
System. String

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase

## INFORMA

## LINKS RELACIONADOS