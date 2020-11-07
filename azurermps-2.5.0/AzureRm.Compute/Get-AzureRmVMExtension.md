---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: ba6d3c19216c8198d4e8cb41fd7fd178cf272ee4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785549"
---
# Get-AzureRmVMExtension

## Sinopse
Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMExtension** Obtém Propriedades de extensões de máquina virtual instaladas em uma máquina virtual.
Especifique o nome de uma extensão para a qual obter as propriedades.
Para obter apenas o modo de exibição de instância de uma extensão, especifique o parâmetro status.

## EXEMPLOS

### Exemplo 1: obter propriedades de uma extensão
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

Este comando obtém as propriedades da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.

### Exemplo 2: obter o modo de exibição de instância de uma extensão
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

Esse comando obtém o modo de exibição de instância da extensão chamada CustomScriptExtension na máquina virtual nomeada VirtualMachine22 no grupo de recursos ResourceGroup11.

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

### -Nome
Especifica o nome de uma extensão.
Esse cmdlet obtém as propriedades da extensão que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Indica que esse cmdlet obtém apenas o modo de exibição de instância de uma extensão.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Especifica o nome de uma máquina virtual.
Esse cmdlet obtém as propriedades de uma extensão da máquina virtual que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmVMExtension](./Remove-AzureRmVMExtension.md)

[Set-AzureRmVMExtension](./Set-AzureRmVMExtension.md)


