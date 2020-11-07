---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: b6ce3afb8b280b9ca07746979f0bb5ba425afd82
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786574"
---
# Get-AzureRmVMCustomScriptExtension

## Sinopse
Obtém informações sobre uma extensão de script personalizada.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMCustomScriptExtension** Obtém informações sobre uma extensão de máquina virtual de script personalizado em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: obter uma extensão de script personalizada
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

Esse comando obtém a extensão de script personalizada chamada ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.

### Exemplo 2: obter o modo de exibição de instância de uma extensão de script personalizado
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

Este comando obtém o modo de exibição de instância da extensão de script personalizado chamado ContosoCustomScript para a máquina virtual nomeada VirtualMachine07.

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
Especifica o nome da extensão de script personalizada sobre a qual esse cmdlet obtém informações.

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
Especifica o nome do grupo de recursos da máquina virtual.

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
Indica que esse cmdlet obtém o modo de exibição de instância da extensão de script personalizado.

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
Especifica o nome de uma máquina virtual para a qual esse cmdlet obtém a extensão de script personalizada.

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

### Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineCustomScriptExtensionContext

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMAccessExtension](./Get-AzureRmVMAccessExtension.md)

[Get-AzureRmVMExtension](./Get-AzureRmVMExtension.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)


