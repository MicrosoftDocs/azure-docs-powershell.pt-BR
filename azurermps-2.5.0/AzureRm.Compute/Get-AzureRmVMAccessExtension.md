---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785554"
---
# Get-AzureRmVMAccessExtension

## Sinopse
Obtém informações sobre a extensão VMAccess.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMAccessExtension** Obtém informações sobre a extensão da máquina virtual do VMAccess (acesso à máquina virtual).

## EXEMPLOS

### Exemplo 1: obter a extensão VMAccess
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

Esse comando obtém a extensão VMAccess chamada ContosoTest para a máquina virtual nomeada VirtualMachine07.

### Exemplo 2: obter o modo de exibição de instância da extensão VMAccess
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

Esse comando obtém o modo de exibição de instância da extensão VMAccess chamada ContosoTest para a máquina virtual chamada VirtualMachine07.

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
Especifica o nome da extensão obtida por esse cmdlet.

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
Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão.

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
Este cmdlet obtém informações sobre VMAccess para a máquina virtual que esse parâmetro especifica.

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

### Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmVMAccessExtension](./Remove-AzureRmVMAccessExtension.md)

[Set-AzureRmVMAccessExtension](./Set-AzureRmVMAccessExtension.md)

[Get-AzureRmVMExtension](./Get-AzureRmVMExtension.md)


