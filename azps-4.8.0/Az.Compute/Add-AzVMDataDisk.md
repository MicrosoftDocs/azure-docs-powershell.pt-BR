---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955982"
---
# Add-AzVMDataDisk

## Sinopse
Adiciona um disco de dados a uma máquina virtual.

## SYNTAX

### VmNormalDiskParameterSetName (padrão)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzVMDataDisk** adiciona um disco de dados a uma máquina virtual.
Você pode adicionar um disco de dados quando cria uma máquina virtual ou pode adicionar um disco de dados a uma máquina virtual existente.

## EXEMPLOS

### Exemplo 1: adicionar discos de dados a uma nova máquina virtual
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.
O comando atribui um nome e um tamanho para a máquina virtual.
Os próximos três comandos atribuem caminhos de três discos de dados às variáveis $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.
Essa abordagem só tem a legibilidade dos comandos a seguir.
Os três comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.
O URI de cada disco é armazenado no $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.

### Exemplo 2: adicionar um disco de dados a uma máquina virtual existente
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet [Get-AzVM](./Get-AzVM.md) .
O comando armazena a máquina virtual na variável $VirtualMachine.
O segundo comando adiciona um disco de dados à máquina virtual armazenada em $VirtualMachine.
O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.

### Exemplo 3: adicionar um disco de dados a uma nova máquina virtual a partir de uma imagem geral do usuário
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e um tamanho para a máquina virtual.
Os próximos dois comandos atribuem caminhos para a imagem de dados e discos de dados às variáveis $DataImageUri e $DataDiskUri, respectivamente.
Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.
Os comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.

### Exemplo 4: adicionar discos de dados a uma nova máquina virtual a partir de uma imagem de usuário especializada
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e um tamanho para a máquina virtual.
Os comandos a seguir atribuirão caminhos do disco de dados à variável $DataDiskUri.
Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.
O comando final adicionar um disco de dados à máquina virtual armazenada em $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.

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
Position: 3
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
Position: 6
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

### -DiskEncryptionSetId
Especifica a ID do recurso do conjunto de criptografia de disco gerenciado pelo cliente.  Só pode ser especificado para disco gerenciado.

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
Especifica o tamanho, em gigabytes, de um disco vazio para ser anexado a uma máquina virtual.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Especifica o número de unidade lógica (LUN) para um disco de dados.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Especifica a ID de um disco gerenciado.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do disco de dados a ser adicionado.

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

### -SourceImageUri
Especifica o URI de origem do disco que este cmdlet anexa.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Especifica o tipo de conta de armazenamento do disco gerenciado.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Especifica o URI (Uniform Resource Identifier) para o arquivo de disco rígido virtual (VHD) a ser criado quando uma imagem de plataforma ou de usuário é usada.
Esse cmdlet copia o blob (objeto grande binário) da imagem para este local.
Este é o local de onde deseja iniciar a máquina virtual.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual local ao qual adicionar um disco de dados.
Você pode usar o cmdlet **Get-AzVM** para obter um objeto de máquina virtual.
Você pode usar o cmdlet **New-AzVMConfig** para criar um objeto de máquina virtual.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

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
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### System. String

### Microsoft. Azure. Management. COMPUTE. Models. CachingTypes

### System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM

## INFORMA

## LINKS RELACIONADOS

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
