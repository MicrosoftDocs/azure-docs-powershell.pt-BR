---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 9c9f7dca5bd698a0eda76637618fe946b723a576
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429850"
---
# Remove-AzureRmVMDiskEncryptionExtension

## Sinopse
Remove a extensão de criptografia de disco de uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmVMDiskEncryptionExtension** remove a extensão de criptografia de disco de uma máquina virtual.
Se nenhum nome de extensão for especificado, esse cmdlet removerá a extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais com base em Linux.
Esse cmdlet não desabilita a criptografia na máquina virtual.
Ele remove a extensão e a configuração de extensão associada da máquina virtual.

## EXEMPLOS

### Exemplo 1: remover a extensão de criptografia de disco de uma máquina virtual.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

Esse comando Remove a extensão com o nome padrão AzureDiskEncryption para uma máquina virtual que executa o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquina virtual com base em Linux chamado MyTestVM.

### Exemplo 2: remover uma extensão de criptografia de disco específica de uma máquina virtual.
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

Esse comando Remove a extensão de criptografia chamada MyDiskEncryptionExtension da máquina virtual nomeada MyTestVM.

## OS

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.
O cmdlet Set-AzureRmVMDiskEncryptionExtension define esse nome para AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows e o AzureDiskEncryptionForLinux para máquinas virtuais Linux.
Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzureRmVMDiskEncryptionExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos para a máquina virtual.

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

### -VMName
Especifica o nome da máquina virtual.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.

O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Set-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


