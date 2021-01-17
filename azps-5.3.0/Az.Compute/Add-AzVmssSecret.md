---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434385"
---
# Add-AzVmssSecret

## Sinopse
Adiciona um segredo a um VMSS.

## SYNTAX

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzVmssSecret** adiciona um segredo ao conjunto de dimensionamento de máquina virtual (VMSS).
O segredo deve ser armazenado em um cofre de chaves do Azure.
Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chave do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) (https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](/powershell/module/az.keyvault) ou o cmdlet [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .

## EXEMPLOS

### Exemplo 1: adicionar um segredo à VMSS
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

Este exemplo adiciona um segredo à VMSS.
O primeiro comando usa o cmdlet Get-AzKeyVault para obter um segredo de cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.
O segundo comando usa o cmdlet **New-AzVmssVaultCertificateConfig** para criar uma configuração de certificado de cofre de chaves usando a URL do certificado especificado do repositório de certificados chamado certificados e armazena os resultados na variável chamada $CertConfig.
O terceiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.
O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID do recurso chave e o certificado do cofre armazenado nas variáveis $Vault e $CertConfig.

## OS

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

### -SourceVaultId
Especifica a ID do recurso do cofre de chaves que contém os certificados que você pode adicionar à máquina virtual.
Esse valor também funciona como a chave para adicionar vários certificados.
Isso significa que você pode usar o mesmo valor para o parâmetro *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.

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

### -VaultCertificate
Especifica o objeto de **certificado** do cofre que contém a URL do certificado e o nome do certificado.
Você pode usar o cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) para criar esse objeto.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
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
Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar esse objeto.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

### System. String

### Microsoft. Azure. Management. COMPUTE. Models. VaultCertificate []

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

## INFORMA

## LINKS RELACIONADOS

[New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)
