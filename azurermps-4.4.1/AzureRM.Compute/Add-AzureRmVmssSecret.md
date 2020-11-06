---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 26811c16f2946b1605c2d3052dc7aca481917d11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609725"
---
# Add-AzureRmVmssSecret

## Sinopse
Adiciona um segredo a um VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVmssSecret** adiciona um segredo ao conjunto de dimensionamento de máquina virtual (VMSS).
O segredo deve ser armazenado em um cofre de chaves do Azure.
Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chave do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) na biblioteca Microsoft Developer Network ou cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## EXEMPLOS

### Exemplo 1: adicionar um segredo à VMSS
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

Este exemplo adiciona um segredo à VMSS.
O primeiro comando usa o cmdlet Get-AzureRmKeyVault para obter um segredo de cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.
O segundo comando usa o cmdlet **New-AzureRmVmssVaultCertificateConfig** para criar uma configuração de certificado de cofre de chaves usando a URL do certificado especificado do repositório de certificados chamado certificados e armazena os resultados na variável chamada $CertConfig.
O terceiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.
O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID do recurso chave e o certificado do cofre armazenado nas variáveis $Vault e $CertConfig.

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

### -SourceVaultId
Especifica a ID do recurso do cofre de chaves que contém os certificados que você pode adicionar à máquina virtual.
Esse valor também funciona como a chave para adicionar vários certificados.
Isso significa que você pode usar o mesmo valor para o parâmetro *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.

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

### -VaultCertificate
Especifica o objeto de **certificado** do cofre que contém a URL do certificado e o nome do certificado.
Você pode usar o cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) para criar esse objeto.

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifica o objeto VMSS.
Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar esse objeto.

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### VirtualMachineScaleSet
O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline

## EXIBE

### Esse cmdlet não gera nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
