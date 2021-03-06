---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 70342620aeab42ba7236091e8aacc32ea44354ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786191"
---
# Add-AzureRmVMSecret

## Sinopse
Adiciona um segredo a uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVMSecret** adiciona um segredo a uma máquina virtual.
Esse valor permite adicionar um certificado à máquina virtual.
O segredo deve ser armazenado em um cofre de chaves.
Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chaves do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) na biblioteca do Microsoft Developer Network ou o cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## EXEMPLOS

### Exemplo 1: adicionar um segredo a uma máquina virtual
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.
O comando atribui um nome e um tamanho para a máquina virtual.

O segundo comando cria um objeto Credential usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.
O comando solicita um nome de usuário e uma senha.
Para obter mais informações, digite `Get-Help Get-Credential` .

O terceiro comando usa o cmdlet **set-AzureRmVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.

O quarto comando atribui uma ID do cofre de origem à variável $SourceVaultId para uso posterior.
O comando pressupõe que a variável $SubscriptionId tem um valor apropriado.

O quinto comando atribui um valor à variável $CertificateStore 01 para uso posterior.

O sexto comando atribui uma URL para um repositório de certificados.

O sétimo comando adiciona um segredo à máquina virtual armazenada em $VirtualMachine.
O parâmetro SourceVaultId especifica o cofre de chaves.
O comando especifica o nome do repositório de certificados e a URL do certificado.
Você pode executar o **Add-AzureRmVMSecret** repetidamente para adicionar segredos para outros certificados.

## OS

### -CertificateStore
Especifica o nome de um repositório de certificados na máquina virtual que executa o sistema operacional Windows.
Esse cmdlet adiciona o certificado à loja que esse parâmetro especifica.
Você só pode especificar esse parâmetro para máquinas virtuais que executam o sistema operacional Windows.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Especifica a URL que aponta para um segredo do cofre de chaves que contém um certificado.

O certificado é a codificação base64 do objeto JSON (JavaScript Object Notation) seguinte, que é codificada em UTF-8:

{"dados": " \<Base64-encoded-file\> ", "tipo de dados": " \<file-format\> ", "senha": " \<pfx-file-password\> "}


Atualmente, dataType aceita somente arquivos. pfx.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Isso significa que você pode usar o mesmo valor para *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual que esse cmdlet modifica.
Para obter um objeto de máquina virtual, use o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .
Você pode usar o cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) para criar um objeto de máquina virtual.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSVirtualMachine
O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
