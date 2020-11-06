---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427470"
---
# Get-AzureRmRecoveryServicesAsrJob

## Sinopse
Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre de serviços de recuperação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByParam (padrão)
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObject
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesAsrJob** Obtém trabalhos do Azure site Recovery.
Você pode usar esse cmdlet para exibir os trabalhos ASR no cofre de serviços de recuperação.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Retorna todos os trabalhos em um objeto ASR específico (referenciar o objeto ASR, como um item replicado ou plano de recuperação por sua ID). 

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

### -EndTime
Especifica a hora de término dos trabalhos.
Esse cmdlet obtém todos os trabalhos que começarem antes do tempo especificado.
Para obter um objeto **DateTime** para esse parâmetro, use o cmdlet Get-Date.
Para obter mais informações, digite `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho
Especifica o objeto de trabalho ASR para o qual obter detalhes atualizados.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifique o trabalho ASR por nome.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Especifica a hora de início dos trabalhos.
Esse cmdlet obtém todos os trabalhos que iniciaram após a hora especificada.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Estado
Especifica o estado para um trabalho ASR.
Esse cmdlet obtém todos os trabalhos que correspondem ao estado especificado.
Os valores aceitáveis para esse parâmetro são:

- Não iniciado
- InProgress
- Foi
- Demais
- Conseguiu
- Cela
- Interrompido

```yaml
Type: String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Especifica a ID do objeto. Usado para pesquisar trabalhos no objeto especificado.

```yaml
Type: String
Parameter Sets: ByParam
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

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob

## EXIBE

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

[Restart-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[Currículo-AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[Parar-AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
