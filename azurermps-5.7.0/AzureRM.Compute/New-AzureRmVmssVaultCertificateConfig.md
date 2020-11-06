---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431716"
---
# New-AzureRmVmssVaultCertificateConfig

## Sinopse
Cria uma configuração de certificado de cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmVmssVaultCertificateConfig** especifica o segredo que precisa ser colocado nas máquinas virtuais do VMSS (conjunto de escala de máquina virtual).
O resultado deste cmdlet destina-se a ser usado com o cmdlet Add-AzureRmVmssSecret.

## EXEMPLOS

### Exemplo 1: criar uma configuração de certificado de cofre de chaves
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

Esse comando cria uma configuração de certificado de cofre de chaves que usa o repositório de certificados chamado mycerts localizado na URL do certificado especificado.

## OS

### -CertificateStore
Especifica o repositório de certificados nas máquinas virtuais no conjunto de escala onde o certificado é adicionado.
Isso só é válido para conjuntos de escala da máquina virtual do Windows.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Especifica o URI de um certificado armazenado no cofre de chaves.

É a codificação base64 do objeto JSON que é codificado em UTF-8:


{"dados": " \<Base64-encoded-certificate\> ", "tipo de dados": "pfx", "senha": " \<pfx-file-password\> "}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

###  
Esse cmdlet não gera nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmVmssSecret](./Add-AzureRmVmssSecret.md)
