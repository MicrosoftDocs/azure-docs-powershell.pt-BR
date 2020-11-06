---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: c4a4aa530f29de93458f618dbf45f639fe873f1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431369"
---
# Add-AzureRmVmssVMDataDisk

## Sinopse
Adiciona um disco de dados a uma VM Vmss.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVmssVMDataDisk** adiciona um disco de dados a uma VM Vmss.

## EXEMPLOS

### Exemplo 1: adicionar um disco de dados gerenciado a uma VM Vmss.
```powershell
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

O primeiro comando obtém um disco gerenciado existente.
O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.
O próximo comando adiciona o disco gerenciado à VM Vmss armazenada localmente em $VmssVM.
O comando final atualiza a VM Vmss com o disco de dados adicionado.

## OS

### -Cache
Especifica o modo de cache do disco.
Os valores aceitáveis para esse parâmetro são:
- ReadOnly
- Leitura
- None o valor padrão é ReadWrite.
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

### -Createoption
Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.
Os valores aceitáveis para esse parâmetro são:
- Liga.
Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.
Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .
O *VhdUri* é tudo que é necessário para que a plataforma do Azure seja a localização do disco rígido virtual (VHD) a ser anexado como um disco de dados à máquina virtual.
- Vazia.
Especifique isso para criar um disco de dados vazio.
- FromImage.
Especifique esta opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.
Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para solicitar à plataforma Azure o local do VHD a ser anexado como um disco de dados.
O parâmetro *VhdUri* é usado como a localização que identifica onde o VHD do disco de dados será armazenado quando for usado pela máquina virtual.

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

### -DiskSizeInGB
Especifica o tamanho, em gigabytes, de um disco vazio para ser anexado a uma máquina virtual.

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
Especifica o número de unidade lógica (LUN) para um disco de dados.

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
Especifica o objeto VM do conjunto de escalas da máquina virtual local ao qual adicionar um disco de dados.
Você pode usar o cmdlet **Get-AzureRmVmssVM** para obter um objeto VM do conjunto de escalas da máquina virtual.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM

### System. Int32

### System. String

### Microsoft. Azure. Management. COMPUTE. Models. CachingTypes

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM

## INFORMA

## LINKS RELACIONADOS
