---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 032c38c3fcc3b09286b795fd3e0efba85e076807
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597513"
---
# Add-AzVmssDataDisk

## Sinopse
Adiciona um disco de dados ao VMSS.

## SYNTAX

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzVmssDataDisk** adiciona um disco de dados à instância do VMSS (conjunto de dimensionamento de máquina virtual).

## EXEMPLOS

### Exemplo 1: adicionar um disco de dados
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

Esse comando adiciona um disco de dados vazio ao objeto VMSS.

## OS

### -Cache
Especifica o tipo de cache do disco.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Createoption
Especifica a opção criar do disco.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DiskSizeGB
Especifica o tamanho do disco em GB.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Especifica o número de unidade lógica do disco.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do disco.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Especifica o tipo de conta de armazenamento do disco.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifique o objeto VMSS.
Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco de dados.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

### System. String

### System. Int32

### System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. CachingTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

## INFORMA

## LINKS RELACIONADOS
