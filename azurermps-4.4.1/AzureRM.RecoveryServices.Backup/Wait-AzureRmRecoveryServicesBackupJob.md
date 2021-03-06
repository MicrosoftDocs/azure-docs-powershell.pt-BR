---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: c4678cfb29d366c5ad855ea86313ea36be35e10b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430671"
---
# Wait-AzureRmRecoveryServicesBackupJob

## Sinopse
Aguarda o término do trabalho de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Wait-AzureRmRecoveryServicesBackupJob** aguarda a conclusão de um trabalho de backup do Azure.
Tarefas de backup podem levar muito tempo.
Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar a conclusão do trabalho antes que ele continue para outras tarefas.

Um script que inclui esse cmdlet pode ser mais simples que um que sonda o serviço de backup para o status do trabalho.

Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.

## EXEMPLOS

### Exemplo 1: Aguarde a conclusão do trabalho
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.

## OS

### -Trabalho
Especifica o trabalho a ser aguardado.
Para obter um objeto **BackupJob** , use o cmdlet Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout
Especifica o tempo máximo, em segundos, que esse cmdlet aguarda para o trabalho terminar.
É recomendável especificar um valor de tempo limite.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Objeto
O parâmetro ' Job ' aceita o valor do tipo ' Object ' da pipeline

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase]

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesBackupJob](./Get-AzureRmRecoveryServicesBackupJob.md)


