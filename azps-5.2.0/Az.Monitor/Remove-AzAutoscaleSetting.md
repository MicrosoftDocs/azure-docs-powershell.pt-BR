---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 1a55ebe8043cf141bffcc0b908061aec56d0387c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262070"
---
# Remove-AzAutoscaleSetting

## Sinopse
Remove uma configuração de autoescala.

## SYNTAX

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzAutoscaleSetting** remove uma configuração de autoescala.
Você deve especificar o nome da configuração e o nome do grupo de recursos ao qual ele está atribuído.
Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.

## EXEMPLOS

### Exemplo 1

Remove uma configuração de autoescala. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Remove-AzAutoscaleSetting -Name 'LogAlertRule1' -ResourceGroupName MyResourceGroup
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Nome
Especifica o nome da configuração de dimensionamento automático a ser removida.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. AzureOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Add-AzAutoscaleSetting](./Add-AzAutoscaleSetting.md)

[Get-AzAutoscaleSetting](./Get-AzAutoscaleSetting.md)


