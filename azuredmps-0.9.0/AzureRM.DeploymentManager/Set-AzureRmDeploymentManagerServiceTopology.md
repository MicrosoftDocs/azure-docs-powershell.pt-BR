---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: 6387e5a2938bdef99e4aea5e93248a0ecf8e8da7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426234"
---
# Set-AzureRmDeploymentManagerServiceTopology

## Sinopse
Atualiza a topologia de serviço.

## SYNTAX

```
Set-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDeploymentManagerServiceTopology** atualiza uma topologia de serviço com o objeto de topologia de serviço especificado.
O cmdlet retorna o objeto de topologia do serviço atualizado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

Esse comando atualiza uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.
O comando retorna o objeto de topologia do serviço atualizado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Outtopology
O objeto de topologia de serviço.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource

## EXIBE

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDeploymentManagerServiceTopology](./New-AzureRmDeploymentManagerServiceTopology.md)

[Get-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)

[Remove-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)