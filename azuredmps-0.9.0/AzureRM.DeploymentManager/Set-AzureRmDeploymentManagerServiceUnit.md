---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425897"
---
# Set-AzureRmDeploymentManagerServiceUnit

## Sinopse
Atualiza uma unidade de serviço.

## SYNTAX

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDeploymentManagerServiceUnit** atualiza uma unidade de serviço com o objeto de unidade de serviço especificado.
O cmdlet retorna o objeto de unidade de serviço atualizado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

Esse comando atualiza uma unidade de serviço cujo nome, nome do serviço, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, ServiceName, Service Topologyname e ResourceGroupName da $serviceUnitObject, respectivamente.
O comando retorna o objeto de unidade de serviço atualizado.

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

### -Enunidade
O objeto de unidade de serviço.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
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

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource

## EXIBE

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDeploymentManagerServiceUnit](./New-AzureRmDeploymentManagerServiceUnit.md)

[Get-AzureRmDeploymentManagerServiceUnit](./Set-AzureRmDeploymentManagerServiceUnit.md)

[Remove-AzureRmDeploymentManagerServiceUnit](./Remove-AzureRmDeploymentManagerServiceUnit.md)