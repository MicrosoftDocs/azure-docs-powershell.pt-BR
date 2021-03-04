---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887574"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Adiciona um disco de dados a uma VM Vmss.

## SINTAXE

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Add-AzVmssVMDataDisk** adiciona um disco de dados a uma VM Vmss.

## EXEMPLOS

### Exemplo 1: Adicionar um disco de dados gerenciado a uma VM Vmss.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

O primeiro comando obtém um disco gerenciado existente.
O próximo comando obtém uma VM Vmss existente dada pelo nome do grupo de recursos, o nome da vmss e a ID da instância.
O próximo comando adiciona o disco gerenciado à VM Vmss armazenada localmente em $VmssVM.
O comando final atualiza a VM Vmss com disco de dados adicionado.

## PARÂMETROS

### -Cache
Especifica o modo de cache do disco.
Os valores aceitáveis para este parâmetro são:
- ReadOnly
- ReadWrite
- Nenhum O valor padrão é ReadWrite.
Alterar esse valor faz com que a máquina virtual seja reiniciada.
Essa configuração afeta a consistência e o desempenho do disco.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou imagem de usuário, cria um disco vazio ou anexa um disco existente.
Os valores aceitáveis para este parâmetro são:
- Anexar.
Especifique essa opção para criar uma máquina virtual a partir de um disco especializado.
Quando você especificar essa opção, não especifique o *parâmetro SourceImageUri.*
O *VhdUri* é tudo o que é necessário para dizer à plataforma do Azure o local do disco rígido virtual (VHD) para anexar como um disco de dados à máquina virtual.
- Vazio.
Especifique isso para criar um disco de dados vazio.
- FromImage.
Especifique essa opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.
Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para dizer à plataforma do Azure o local do VHD a ser anexado como um disco de dados.
O *parâmetro VhdUri* é usado como o local que identifica onde o VHD do disco de dados será armazenado quando for usado pela máquina virtual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -DiskEncryptionSetId
Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.  Isso só pode ser especificado para disco gerenciado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
Especifica o tamanho, em gigabytes, de um disco vazio a ser anexado a uma máquina virtual.

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

### -Lun
Especifica o número da unidade lógica (LUN) para um disco de dados.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Especifica a ID de um disco gerenciado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Especifica o tipo de conta de armazenamento do disco gerenciado.

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

### -VirtualMachineScaleSetVM
Especifica o objeto VM de conjunto de escala de máquina virtual local ao qual adicionar um disco de dados.
Você pode usar o cmdlet **Get-AzVmssVM** para obter um objeto VM de conjunto de escala de máquina virtual.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Especifica se WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTES

## LINKS RELACIONADOS
