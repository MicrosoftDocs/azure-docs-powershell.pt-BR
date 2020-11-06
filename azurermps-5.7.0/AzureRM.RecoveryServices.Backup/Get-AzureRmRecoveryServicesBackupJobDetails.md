---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427499"
---
# Get-AzureRmRecoveryServicesBackupJobDetails

## Sinopse
Obtém detalhes para um trabalho de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### JobFilterSet (padrão)
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFilterSet
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.

Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.

## EXEMPLOS

### Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

O primeiro comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.

O segundo comando obtém os detalhes do trabalho para os trabalhos com falha no $Jobs e, em seguida, armazena-os na variável $JobDetails.

O comando final exibe detalhes do erro para os trabalhos com falha.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho
Especifica o trabalho a obter.
Para obter um objeto **BackupJob** , use o cmdlet Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Especifica a ID de um trabalho de backup.
A ID é a propriedade InstanceId de um objeto **BackupJob** .

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesBackupJob](./Get-AzureRmRecoveryServicesBackupJob.md)


