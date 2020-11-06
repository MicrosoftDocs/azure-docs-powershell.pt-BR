---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430519"
---
# Get-AzureRmVMDiskEncryptionStatus

## Sinopse
Obtém o status de criptografia da máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMDiskEncryptionStatus** Obtém o status de criptografia da máquina virtual.
Ele exibe o status de criptografia do sistema operacional e dos volumes de dados.
Além do status de criptografia, ele também exibe a URL de segredo de criptografia, a URL da chave de criptografia de chave, as IDs de recurso dos **cofres** de chaves onde a chave de criptografia e a chave de criptografia de chave do volume do sistema operacional estão presentes.

## EXEMPLOS

### Exemplo 1: obter o status de criptografia de uma máquina virtual
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

Esse comando obtém o status de criptografia da máquina virtual chamada VM001.

## OS

### -Nome
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmVMDiskEncryptionExtension](./Remove-AzureRmVMDiskEncryptionExtension.md)

[Set-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


