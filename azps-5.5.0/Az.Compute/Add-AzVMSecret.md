---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116557"
---
# Add-AzVMSecret

## Sinopse
Adiciona um segredo a uma máquina virtual.

## Sintaxe

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Add-AzVMSecsecduto** adiciona um segredo a uma máquina virtual.
Esse valor permite adicionar um certificado à máquina virtual.
O segredo deve ser armazenado em um Cofre de Teclas.
Para saber mais sobre o Cofre de Teclas, confira [o que é o Cofre de Teclas do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Para obter mais informações sobre os cmdlets, consulte [Cmdlets](/powershell/module/az.keyvault) do Cofre de Tecla do Azure ou o cmdlet [Set-AzKeyVaultSec ltd.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## Exemplos

### Exemplo 1: Adicionar um segredo a uma máquina virtual
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

O primeiro comando cria um objeto virtual de máquina e, em seguida, o armazena na variável $VirtualMachine dados.
O comando atribui um nome e um tamanho à máquina virtual.
O segundo comando cria um objeto de credencial usando o cmdlet Get-Credential e armazena o resultado na variável $Credential dados.
O comando solicita um nome de usuário e uma senha.
Para obter mais informações, digite `Get-Help Get-Credential` .
O terceiro comando usa **o cmdlet Set-AzVMOperatingSystem** para configurar a máquina virtual armazenada no $VirtualMachine.
O quarto comando atribui uma ID do cofre de origem à variável $SourceVaultId para uso posterior.
O comando supõe que a variável $SubscriptionId tenha um valor apropriado.
O quinto comando atribui um valor à variável $CertificateStore 01 para uso posterior.
O sexto comando atribui uma URL para um armazenamento de certificados.
O sétimo comando adiciona um segredo à máquina virtual armazenada $VirtualMachine.
O parâmetro SourceVaultId especifica o Cofre de Teclas.
O comando especifica o nome do armazenamento de certificados e a URL do certificado.
Você pode executar o **Add-AzVMSecsec repetidamente** para adicionar segredos para outros certificados.

## Parâmetros

### -CertificateStore
Especifica o nome de um armazenamento de certificados no computador virtual que executa o sistema operacional Windows.
Este cmdlet adiciona o certificado ao armazenamento especificado por esse parâmetro.
Você só pode especificar esse parâmetro para máquinas virtuais que executem o sistema operacional Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Especifica a URL que aponta para um segredo do Cofre de Chave que contém um certificado.
O certificado é a codificação Base64 do seguinte objeto JSON (JavaScript Object Notation), codificado em UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } Atualmente, dataType aceita apenas arquivos \<pfx-file-password\> .pfx.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### -SourceVaultId
Especifica a ID de recurso do Cofre de Teclas que contém os certificados que você pode adicionar à máquina virtual.
Esse valor também funciona como a chave para adicionar vários certificados.
Isso significa que você pode usar o mesmo valor para *SourceVaultId* ao adicionar vários certificados do mesmo Cofre de Teclas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto de máquina virtual que este cmdlet modifica.
Para obter um objeto de máquina virtual, use [o cmdlet Get-AzVM.](./Get-AzVM.md)
Você pode usar o [cmdlet New-AzVMConfig](./New-AzVMConfig.md) para criar um objeto de máquina virtual.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## Saídas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## Notas

## LINKS RELACIONADOS

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
