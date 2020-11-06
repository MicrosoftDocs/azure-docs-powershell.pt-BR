---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428555"
---
# Get-AzureRmVM

## Sinopse
Obtém as propriedades de uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ListAllVirtualMachinesParamSet (padrão)
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListLocationVirtualMachinesParamSet
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVM** Obtém o modo de exibição de modelo e o modo de exibição de instância de uma máquina virtual do Azure.
O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.
O modo de exibição de instância é o status do nível de instância da máquina virtual.
Especifique o parâmetro *status* para obter apenas o modo de exibição de instância de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.

### Exemplo 2: obter propriedades do modo de exibição de instância
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.
Esse comando especifica o parâmetro *status* .
Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.

### Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.

### Exemplo 4: obter todas as máquinas virtuais na sua assinatura
```
PS C:\> Get-AzureRmVM
```

Este comando obtém todas as máquinas virtuais na sua assinatura.

### Exemplo 5: obter todas as máquinas virtuais no local.
```
PS C:\> Get-AzureRmVM -Location "westus"
```

Esse comando obtém todas as máquinas virtuais na região oeste dos EUA.

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

### -DisplayHint
Determina como o objeto de máquina virtual é exibido.
Os valores válidos são:--Compact: exibe apenas as propriedades de nível superior--expande: exibe todas as propriedades em todos os níveis

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica um local para as máquinas virtuais a serem listadas.

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da máquina virtual a ser obtida.

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Especifica o próximo link.

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. URI

### Microsoft. Azure. Commands. COMPUTE. Models. DisplayHintType

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmVM](./New-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Restart-AzureRmVM](./Restart-AzureRmVM.md)

[Start-AzureRmVM](./Start-AzureRmVM.md)

[Parar-AzureRmVM](./Stop-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


