---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428593"
---
# Wait-AzureRmBackupJob

## Sinopse
Aguarda o término do trabalho de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Wait-AzureRmBackupJob** aguarda a conclusão de um trabalho de backup do Azure.
Tarefas de backup podem levar muito tempo.
Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar a conclusão do trabalho antes que ele continue para outras tarefas.
Um script que inclui esse cmdlet pode ser mais simples que um que sonda o serviço de backup para o status do trabalho.

## EXEMPLOS

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Trabalho
Especifica um trabalho cancelado por esse cmdlet.
Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeOut
Especifica o tempo máximo, em segundos, que esse cmdlet aguarda para o trabalho terminar.
Recomendamos que você especifique um valor de tempo limite.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. Object
Parâmetros: Job (ByValue)

## EXIBE

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Parar-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)


