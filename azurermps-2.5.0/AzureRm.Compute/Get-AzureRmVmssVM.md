---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: bac1bf365ff1135366f2612bfbe5ba313e2300b8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786564"
---
# Get-AzureRmVmssVM

## Sinopse
Obtém as propriedades de uma máquina virtual VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Defaultparameter (padrão)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVmssVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de um computador virtual de faixa de máquina virtual (VMSS).
O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.
O modo de exibição de instância é o status do nível de instância da máquina virtual.
Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: obter as propriedades de uma máquina virtual VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS001 que pertence ao grupo de recursos chamado Group001.
Como o comando não especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de modelo da máquina virtual.

### Exemplo 2: obter as propriedades do modo de exibição de modelo de uma máquina virtual VMSS
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de modelo.

### Exemplo 3: obter as propriedades do modo de exibição de instância de uma máquina virtual VMSS
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Esse comando obtém as propriedades da máquina virtual VMSS chamada VMSS004 que pertence ao grupo de recursos chamado Group002.
Como o comando especifica o parâmetro de opção *InstanceView* , o cmdlet obtém o modo de exibição de instância da máquina virtual.
O comando obtém a ID da instância armazenada na variável $ID para a qual obter o modo de exibição de instância.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -InstanceId
Especifica a ID da instância para a qual obter o modo de exibição de modelo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.

```yaml
Type: SwitchParameter
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
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

### Esse cmdlet não gera nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


