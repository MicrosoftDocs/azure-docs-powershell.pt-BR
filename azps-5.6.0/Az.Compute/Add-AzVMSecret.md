---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886694"
---
# <span data-ttu-id="e67bb-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="e67bb-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="e67bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e67bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e67bb-103">Adiciona um segredo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="e67bb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e67bb-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e67bb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e67bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e67bb-106">O cmdlet **Add-AzVMSecret** adiciona um segredo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="e67bb-107">Esse valor permite adicionar um certificado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="e67bb-108">O segredo deve ser armazenado em um Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="e67bb-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="e67bb-109">Para obter mais informações sobre o Key Vault, consulte [O que é o Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="e67bb-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="e67bb-110">Para obter mais informações sobre os cmdlets, consulte [Cmdlets do Azure Key Vault](/powershell/module/az.keyvault) ou o cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="e67bb-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="e67bb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e67bb-111">EXAMPLES</span></span>

### <span data-ttu-id="e67bb-112">Exemplo 1: Adicionar um segredo a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e67bb-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="e67bb-113">O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e67bb-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e67bb-114">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e67bb-115">O segundo comando cria um objeto de credencial usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="e67bb-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="e67bb-116">O comando solicita um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="e67bb-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="e67bb-117">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e67bb-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="e67bb-118">O terceiro comando usa o cmdlet **Set-AzVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e67bb-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e67bb-119">O quarto comando atribui uma ID do cofre de origem à variável $SourceVaultId para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="e67bb-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="e67bb-120">O comando assume que a variável $SubscriptionId tem um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="e67bb-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="e67bb-121">O quinto comando atribui um valor à variável $CertificateStore 01 para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="e67bb-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="e67bb-122">O sexto comando atribui uma URL para um armazenamento de certificados.</span><span class="sxs-lookup"><span data-stu-id="e67bb-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="e67bb-123">O sétimo comando adiciona um segredo à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e67bb-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e67bb-124">O parâmetro SourceVaultId especifica o Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="e67bb-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="e67bb-125">O comando especifica o nome do armazenamento de certificados e a URL do certificado.</span><span class="sxs-lookup"><span data-stu-id="e67bb-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="e67bb-126">Você pode executar o **Add-AzVMSecret** repetidamente para adicionar segredos para outros certificados.</span><span class="sxs-lookup"><span data-stu-id="e67bb-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="e67bb-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e67bb-127">PARAMETERS</span></span>

### <span data-ttu-id="e67bb-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="e67bb-128">-CertificateStore</span></span>
<span data-ttu-id="e67bb-129">Especifica o nome de um armazenamento de certificados na máquina virtual que executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="e67bb-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="e67bb-130">Este cmdlet adiciona o certificado ao armazenamento especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e67bb-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="e67bb-131">Você só pode especificar esse parâmetro para máquinas virtuais que executem o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="e67bb-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="e67bb-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e67bb-132">-CertificateUrl</span></span>
<span data-ttu-id="e67bb-133">Especifica a URL que aponta para um segredo do Cofre de Chaves que contém um certificado.</span><span class="sxs-lookup"><span data-stu-id="e67bb-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="e67bb-134">O certificado é a codificação Base64 do seguinte objeto JavaScript Object Notation (JSON), que é codificado em UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } Atualmente, dataType aceita apenas arquivos \<pfx-file-password\> .pfx.</span><span class="sxs-lookup"><span data-stu-id="e67bb-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="e67bb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67bb-135">-DefaultProfile</span></span>
<span data-ttu-id="e67bb-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e67bb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e67bb-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e67bb-137">-SourceVaultId</span></span>
<span data-ttu-id="e67bb-138">Especifica a ID de recurso do Cofre de Chaves que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="e67bb-139">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="e67bb-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="e67bb-140">Isso significa que você pode usar o mesmo valor para *SourceVaultId* quando adicionar vários certificados do mesmo Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="e67bb-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="e67bb-141">-VM</span><span class="sxs-lookup"><span data-stu-id="e67bb-141">-VM</span></span>
<span data-ttu-id="e67bb-142">Especifica o objeto de máquina virtual que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e67bb-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="e67bb-143">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="e67bb-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="e67bb-144">Você pode usar o cmdlet [New-AzVMConfig](./New-AzVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e67bb-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="e67bb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67bb-145">CommonParameters</span></span>
<span data-ttu-id="e67bb-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67bb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67bb-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e67bb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67bb-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e67bb-148">INPUTS</span></span>

### <span data-ttu-id="e67bb-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e67bb-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e67bb-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e67bb-150">System.String</span></span>

## <span data-ttu-id="e67bb-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e67bb-151">OUTPUTS</span></span>

### <span data-ttu-id="e67bb-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e67bb-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e67bb-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="e67bb-153">NOTES</span></span>

## <span data-ttu-id="e67bb-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e67bb-154">RELATED LINKS</span></span>

[<span data-ttu-id="e67bb-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e67bb-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e67bb-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e67bb-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="e67bb-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e67bb-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
