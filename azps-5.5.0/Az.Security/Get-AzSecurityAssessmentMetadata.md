---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116201"
---
# Get-AzSecurityAssessmentMetadata

## Sinopse
Obtém tipos de avaliações de segurança e metadta em uma assinatura.

## Sintaxe

### SubscriptionScope (Padrão)
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceid
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
Obtém tipos de avaliações de segurança e metadta em uma assinatura. Os metadados da Avaliação de Built-In incluem avaliações e tipos de avaliação personalizados que o usuário pode definir.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

Obtém todas as avaliações internas e as avaliações personalizadas que foram configuradas na assinatura atual.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do recurso.

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso de segurança em que você deseja invocar o comando.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata

## Notas

## LINKS RELACIONADOS
