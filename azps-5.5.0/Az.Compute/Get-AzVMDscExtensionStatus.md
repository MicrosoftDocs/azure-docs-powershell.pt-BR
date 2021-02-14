---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: b932c7e6f920d538e501b584395f41ce2089b5de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115478"
---
# Get-AzVMDscExtensionStatus

## Sinopse
Obtém o status do manipulador de extensão DSC para uma máquina virtual.

## Sintaxe

### GetDscExtension (Padrão)
```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VMParameterSet
```
Get-AzVMDscExtensionStatus [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzVMDscExtensionStatus** obtém o status do manipulador de extensão Configuração de Estado Desejado (DSC) para uma máquina virtual em um grupo de recursos.
Quando uma configuração é aplicada, esse cmdlet produz uma saída consistente com Start-DscConfiguration cmdlet.

## Exemplos

### Exemplo 1

Obtém o status do manipulador de extensão DSC para uma máquina virtual. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -Nome
Especifica o nome do recurso gerenciador de recursos do Azure que representa a extensão.
O cmdlet Set-AzVMDscExtension define esse nome para Microsoft.Powershell.DSC, que é o mesmo valor usado por **Get-AzVMDscExtensionStatus.**
Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet Definir ou usado um nome de recurso diferente em um modelo do Gerenciador de Recursos.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto de máquina virtual em que a extensão está.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName
Especifica o nome de uma máquina virtual para a qual este cmdlet obtém o status da extensão DSC.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView

## Notas

## LINKS RELACIONADOS

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


