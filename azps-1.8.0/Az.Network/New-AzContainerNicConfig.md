---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 18d5891e07dd9d0f9916ebf43e8967152e2c9cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600364"
---
# New-AzContainerNicConfig

## Sinopse
Cria um novo objeto de configuração de interface de rede de contêiner.

## SYNTAX

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzContainerNicConfig** cria um novo objeto de configuração de interface de rede de contêiner. Esse objeto determina as características de interfacs de rede de contêiner criadas para fazer referência ao perfil de rede pai.

## EXEMPLOS

### Exemplo 1
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

O primeiro comando cria uma configuração de interface de rede de contêiner vazia. O segundo cria um novo perfil de rede, passando a configuração da interface de rede de contêiner anteriormente criada como um argumento para o cmdlet New-NetworkProfile.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -IpConfiguration
Coleção de perfis de configuração de IP que determinam quais configurações de IP são criadas quando uma NIC de contêiner é instanciada nesta configuração de interface de rede de contêiner

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome da configuração da interface de rede do contêiner.

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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration

## INFORMA

## LINKS RELACIONADOS

[New-AzContainerNicConfigIpConfig](./New-AzContainerNicConfigIpConfig.md)
