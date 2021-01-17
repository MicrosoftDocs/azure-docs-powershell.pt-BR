---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434330"
---
# Get-AzVmssVM

## Sinopse
Obtém as propriedades de uma máquina virtual VMSS.

## SYNTAX

### Defaultparameter (padrão)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzVmssVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de um computador virtual de faixa de máquina virtual (VMSS).
O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.
O modo de exibição de instância é o status do nível de instância da máquina virtual.
Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: obter as propriedades de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.
Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.

### Exemplo 2: obter as propriedades do modo de exibição de modelo de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de modelo.

### Exemplo 3: obter as propriedades do modo de exibição de instância de uma máquina virtual VMSS
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
Como o comando especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de instância da máquina virtual.
O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de instância.

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

### -InstanceId
Especifica a ID da instância para a qual obter o modo de exibição de modelo.

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
Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.

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
Especifica o nome do grupo de recursos do VMSS.

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
Especifica o nome do VMSS.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM

## INFORMA

## LINKS RELACIONADOS

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


