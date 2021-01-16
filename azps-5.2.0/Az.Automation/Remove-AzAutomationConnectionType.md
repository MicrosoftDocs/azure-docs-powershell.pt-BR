---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264526"
---
# Remove-AzAutomationConnectionType

## Sinopse
Remove um tipo de conexão de automação.

## SYNTAX

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzAutomationConnectionType** remove um tipo de conexão da automação do Azure.
Todas as conexões associadas ao tipo de conexão que você exclui se tornam inutilizáveis.
Remova-os, a menos que você crie um novo tipo de conexão que atenda aos seguintes critérios: 
- O tipo tem o mesmo nome que o tipo de conexão original. 
- O tipo tem as mesmas definições de campo que o tipo de conexão original.
Ele pode ter campos adicionais.

## EXEMPLOS

### Exemplo 1: remover um tipo de conexão
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

Esse comando Remove um tipo de conexão chamado ContosoConnectionType na conta de automação chamada Contoso17.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação para a qual esse cmdlet Remove um tipo de conexão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do tipo de conexão de automação que este cmdlet Remove.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um tipo de conexão de automação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Remove-AzAutomationConnection](./Remove-AzAutomationConnection.md)


