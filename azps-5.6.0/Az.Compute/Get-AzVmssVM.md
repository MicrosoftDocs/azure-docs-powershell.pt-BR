---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891875"
---
# Get-AzVmssVM

## SYNOPSIS
Obtém as propriedades de uma máquina virtual VMSS.

## SINTAXE

### DefaultParameter (Padrão)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzVmssVM** obtém a exibição de modelo e a exibição de instância de uma máquina virtual VMSS (Conjunto de Escala de Máquina Virtual).
O modelo de exibição é as propriedades especificadas pelo usuário da máquina virtual.
O exemplo de exibição é o status de nível de instância da máquina virtual.
*Especifique o parâmetro Status* para obter apenas a exibição de instância de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: Obter as propriedades de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.
Como o comando não especifica o parâmetro de opção *InstanceView,* o cmdlet obtém a exibição de modelo da máquina virtual.

### Exemplo 2: Obter as propriedades de exibição de modelo de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
O comando obtém a ID da instância armazenada na variável $ID para obter o exibição do modelo.

### Exemplo 3: Obter as propriedades de exibição de instância de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Este comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
Como o comando especifica o parâmetro de opção *InstanceView,* o cmdlet obtém a exibição de instância da máquina virtual.
O comando obtém a ID da instância armazenada na variável $ID para obter o exibição de instância.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -InstanceId
Especifica a ID da instância para a qual obter o modelo de exibição.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Indica que esse cmdlet obtém apenas a exibição de instância da máquina virtual.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do Grupo de Recursos do VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Especiem o nome do VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTES

## LINKS RELACIONADOS

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


