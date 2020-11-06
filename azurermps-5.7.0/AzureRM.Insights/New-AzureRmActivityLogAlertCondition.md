---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: d9309f2de88dc87368b510cdf6f1062d03c7f709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430479"
---
# New-AzureRmActivityLogAlertCondition

## Sinopse
Cria um novo objeto de condição de alerta de log de atividades na memória.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmActivityLogAlertCondition** cria novo objeto de condição de alerta de log de atividades na memória.

## EXEMPLOS

### Exemplo 1: criar um novo objeto de condição de alerta de log de atividades na memória.
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

Esse comando cria um novo objeto de condição de alerta de log de atividades na memória.

**Observação** : quando esse cmdlet é usado com Set-AzureRmActivityLogAlert pelo menos um desses objetos, passados como parâmetros, deve ter seu campo igual a "categoria". Caso contrário, o back-end responderá com um 400 (BadRequest.)

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Igual
Especifica a propriedade Equals para a condição de folha.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Campo
Especifica o campo para a condição.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition

## INFORMA

## LINKS RELACIONADOS

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Enable-AzureRmActivityLogAlert](./Enable-AzureRmActivityLogAlert.md)

[Disable-AzureRmActivityLogAlert](./Disable-AzureRmActivityLogAlert.md)

[Get-AzureRmActivityLogAlert](./Get-AzureRmActivityLogAlert.md)

[Remove-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[New-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
