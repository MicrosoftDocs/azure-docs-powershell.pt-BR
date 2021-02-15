---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112834"
---
# New-AzFirewallPolicyIntrusionDetectionSignatureOverride

## Sinopse
Cria uma nova Substituição de Assinatura de Detecção de Invasão de Política de Firewall do Azure

## Sintaxe

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cria um Objeto de Substituição de Assinatura de Política de Firewall do Azure.

## Exemplos

### Exemplo 1: 1. Criar detecção de invasão com substituições de assinatura
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
Este exemplo cria a detecção de invasão com substituição de assinatura específica para o modo Negar

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

### -ID
ID da assinatura.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Modo
Estado da assinatura.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride

## Notas

## LINKS RELACIONADOS
