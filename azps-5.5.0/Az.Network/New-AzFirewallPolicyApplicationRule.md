---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112842"
---
# New-AzFirewallPolicyApplicationRule

## Sinopse
Criar uma nova Regra de Aplicativo de Política de Firewall do Azure

## Sintaxe

### SourceAddressAndTargetFqdn (Padrão)
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceAddressAndFqdnTag
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceAddressAndWebCategory
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceAddressAndTargetUrl
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndTargetUrl
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndTargetFqdn
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndFqdnTag
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SourceIpGroupAndWebCategory
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzFirewallPolicyApplicationRule** cria uma Regra de Aplicativo para uma Política de Firewall do Azure.

## Exemplos

### Exemplo 1
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

Este exemplo cria uma regra de aplicativo com o endereço de origem, o protocolo e os fqdns de destino.

### Exemplo 2
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

Este exemplo cria uma regra de aplicativo com o endereço de origem, protocolo e categorias da Web.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Descrição
A descrição da regra

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FqdnTag
As Marcas FQDN da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome da Regra de Aplicativo

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Os protocolos da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Os endereços de origem da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceIpGroup
Os grupos ipgroups de origem da regra

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFqdn
Os FQDNs de destino da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebCategory
As Categorias Da Web da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetUrl
A Url de Destino da regra

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TerminateTLS
Indica o encerramento de TLS

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

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

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule

## Notas

## LINKS RELACIONADOS
