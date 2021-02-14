---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116559"
---
# Add-AzVMDataDisk

## Sinopse
Adiciona um disco de dados a uma máquina virtual.

## Sintaxe

### VmNormalDiskParameterSetName (Padrão)
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

## Descrição
O **cmdlet Add-AzVMDataDisk** adiciona um disco de dados a uma máquina virtual.
Você pode adicionar um disco de dados ao criar uma máquina virtual ou pode adicionar um disco de dados a uma máquina virtual existente.

## Exemplos

### Exemplo 1: Adicionar discos de dados a uma nova máquina virtual
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

O primeiro comando cria um objeto virtual de máquina e, em seguida, o armazena na variável $VirtualMachine dados.
O comando atribui um nome e um tamanho à máquina virtual.
Os três comandos a seguir atribuem caminhos de três discos de dados às variáveis $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.
Esta abordagem é apenas para a capacidade de leitura dos comandos a seguir.
Os três comandos finais adicionam um disco de dados à máquina virtual armazenada $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.
O URI de cada disco é armazenado em $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.

### Exemplo 2: Adicionar um disco de dados a uma máquina virtual existente
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet [Get-AzVM.](./Get-AzVM.md)
O comando armazena a máquina virtual na variável $VirtualMachine dados.
O segundo comando adiciona um disco de dados à máquina virtual armazenada $VirtualMachine.
O comando final atualiza o estado da máquina virtual armazenada $VirtualMachine no ResourceGroup11.

### Exemplo 3: Adicionar um disco de dados a uma nova máquina virtual a partir de uma imagem de usuário generalizada
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

O primeiro comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.
O comando atribui um nome e um tamanho à máquina virtual.
Os próximos dois comandos atribuem caminhos para a imagem de dados e discos de dados para as variáveis $DataImageUri e $DataDiskUri, respectivamente.
Essa abordagem é usada para melhorar a capacidade de leitura dos comandos a seguir.
Os comandos finais adicionam um disco de dados à máquina virtual armazenada $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.

### Exemplo 4: Adicionar discos de dados a uma nova máquina virtual a partir de uma imagem de usuário especializada
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

O primeiro comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.
O comando atribui um nome e um tamanho à máquina virtual.
Os próximos comandos atribuem caminhos do disco de dados à variável $DataDiskUri dados.
Essa abordagem é usada para melhorar a capacidade de leitura dos comandos a seguir.
O comando final adiciona um disco de dados à máquina virtual armazenada $VirtualMachine.
O comando especifica o nome e o local do disco e outras propriedades do disco.

## Parâmetros

### -Cache
Especifica o modo de cache do disco.
Os valores aceitáveis para este parâmetro são:
- Readonly
- Readwrite
- Nenhum O valor padrão é ReadWrite.
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

### -CreateOption
Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário, cria um disco vazio ou anexa um disco existente.
Os valores aceitáveis para este parâmetro são:
- Anexar.
Especifique essa opção para criar uma máquina virtual a partir de um disco especializado.
Quando você especificar essa opção, não especifique o parâmetro *SourceImageUri.*
O *LtdadUri* é tudo o que é necessário para dizer à plataforma do Azure o local do disco rígido virtual (TEMD) a ser anexado como um disco de dados à máquina virtual.
- Vazio.
Especifique isso para criar um disco de dados vazio.
- Fromimage.
Especifique essa opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.
Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para dizer à plataforma do Azure o local da d'água para anexar como um disco de dados.
O *parâmetro LtdadUri* é usado como o local que identifica onde o disco de dados TEMD será armazenado quando for usado pela máquina virtual.

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
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ltda
Especifica o número de unidade lógica (NUMD) de um disco de dados.

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
Especifica o nome do disco de dados a ser acrescentado.

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

### -HighdUri
Especifica o URI (Uniform Resource Identifier) do arquivo de disco rígido virtual (PGD) a ser criado quando uma imagem de usuário ou imagem de plataforma é usada.
Este cmdlet copia o objeto binário de imagem grande (blob) para esse local.
Este é o local de onde iniciar a máquina virtual.

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
Especifica o objeto de máquina virtual local ao qual adicionar um disco de dados.
Você pode usar o **cmdlet Get-AzVM** para obter um objeto de máquina virtual.
Você pode usar o **cmdlet New-AzVMConfig** para criar um objeto de máquina virtual.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## Saídas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## Notas

## LINKS RELACIONADOS

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
