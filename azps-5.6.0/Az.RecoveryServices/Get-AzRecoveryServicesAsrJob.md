---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 8f9f16b0f5ea4b36cfe8247eed2ed6e88ecd4853
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888199"
---
# Get-AzRecoveryServicesAsrJob

## SYNOPSIS
Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre dos Serviços de Recuperação.

## SINTAXE

### ByParam (Padrão)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzRecoveryServicesAsrJob** obtém trabalhos de Recuperação de Site do Azure.
Você pode usar esse cmdlet para exibir os trabalhos ASR no cofre dos Serviços de Recuperação.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Retorna todos os trabalhos em um objeto ASR específico(referência ao objeto ASR, como item replicado ou plano de recuperação por sua ID.) 

### Exemplo 2

Obtém os detalhes do trabalho ASR especificado ou a lista de trabalhos ASR recentes no cofre dos Serviços de Recuperação. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrJob -Job $Job
```

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.


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

### -EndTime
Especifica a hora de término dos trabalhos.
Este cmdlet obtém todos os trabalhos iniciados antes do horário especificado.
Para obter um **objeto DateTime** para esse parâmetro, use Get-Date cmdlet.
Para obter mais informações, digite `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Especifica o objeto de trabalho ASR para obter detalhes atualizados.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Especifique o trabalho ASR pelo nome.

```yaml
Type: System.String
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
Este cmdlet obtém todos os trabalhos iniciados após o horário especificado.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Especifica o estado de um trabalho ASR.
Este cmdlet obtém todos os trabalhos que corresponderem ao estado especificado.
Os valores aceitáveis para este parâmetro são:

- NotStarted
- InProgress
- Bem-sucedido
- Outros
- Falha
- Cancelado
- Suspenso

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## SAÍDAS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## NOTES

## LINKS RELACIONADOS

[Restart-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[Stop-AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
