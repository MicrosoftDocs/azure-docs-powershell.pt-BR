---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSecret.md
ms.openlocfilehash: 517614e93510aab163f5d632705e4a5a3566186a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429881"
---
# <span data-ttu-id="2424e-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="2424e-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="2424e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2424e-102">SYNOPSIS</span></span>
<span data-ttu-id="2424e-103">Adiciona um segredo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2424e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2424e-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2424e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2424e-105">DESCRIPTION</span></span>
<span data-ttu-id="2424e-106">O cmdlet **Add-AzureRmVMSecret** adiciona um segredo a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="2424e-107">Esse valor permite adicionar um certificado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="2424e-108">O segredo deve ser armazenado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2424e-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="2424e-109">Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chaves do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="2424e-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="2424e-110">Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) na biblioteca do Microsoft Developer Network ou o cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="2424e-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="2424e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2424e-111">EXAMPLES</span></span>

### <span data-ttu-id="2424e-112">Exemplo 1: adicionar um segredo a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="2424e-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="2424e-113">O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2424e-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2424e-114">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="2424e-115">O segundo comando cria um objeto Credential usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="2424e-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="2424e-116">O comando solicita um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="2424e-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="2424e-117">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="2424e-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="2424e-118">O terceiro comando usa o cmdlet **set-AzureRmVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2424e-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="2424e-119">O quarto comando atribui uma ID do cofre de origem à variável $SourceVaultId para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="2424e-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="2424e-120">O comando pressupõe que a variável $SubscriptionId tem um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="2424e-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="2424e-121">O quinto comando atribui um valor à variável $CertificateStore 01 para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="2424e-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="2424e-122">O sexto comando atribui uma URL para um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="2424e-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="2424e-123">O sétimo comando adiciona um segredo à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2424e-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2424e-124">O parâmetro SourceVaultId especifica o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2424e-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="2424e-125">O comando especifica o nome do repositório de certificados e a URL do certificado.</span><span class="sxs-lookup"><span data-stu-id="2424e-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="2424e-126">Você pode executar o **Add-AzureRmVMSecret** repetidamente para adicionar segredos para outros certificados.</span><span class="sxs-lookup"><span data-stu-id="2424e-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="2424e-127">OS</span><span class="sxs-lookup"><span data-stu-id="2424e-127">PARAMETERS</span></span>

### <span data-ttu-id="2424e-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="2424e-128">-CertificateStore</span></span>
<span data-ttu-id="2424e-129">Especifica o nome de um repositório de certificados na máquina virtual que executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2424e-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="2424e-130">Esse cmdlet adiciona o certificado à loja que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2424e-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="2424e-131">Você só pode especificar esse parâmetro para máquinas virtuais que executam o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2424e-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="2424e-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="2424e-132">-CertificateUrl</span></span>
<span data-ttu-id="2424e-133">Especifica a URL que aponta para um segredo do cofre de chaves que contém um certificado.</span><span class="sxs-lookup"><span data-stu-id="2424e-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="2424e-134">O certificado é a codificação base64 do objeto JSON (JavaScript Object Notation) seguinte, que é codificada em UTF-8:</span><span class="sxs-lookup"><span data-stu-id="2424e-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="2424e-135">{"dados": " \<Base64-encoded-file\> ", "tipo de dados": " \<file-format\> ", "senha": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="2424e-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="2424e-136">Atualmente, dataType aceita somente arquivos. pfx.</span><span class="sxs-lookup"><span data-stu-id="2424e-136">Currently, dataType accepts only .pfx files.</span></span>

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

### <span data-ttu-id="2424e-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="2424e-137">-SourceVaultId</span></span>
<span data-ttu-id="2424e-138">Especifica a ID do recurso do cofre de chaves que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="2424e-139">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="2424e-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="2424e-140">Isso significa que você pode usar o mesmo valor para *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2424e-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="2424e-141">-VM</span><span class="sxs-lookup"><span data-stu-id="2424e-141">-VM</span></span>
<span data-ttu-id="2424e-142">Especifica o objeto da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2424e-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="2424e-143">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="2424e-143">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="2424e-144">Você pode usar o cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2424e-144">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="2424e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2424e-145">CommonParameters</span></span>
<span data-ttu-id="2424e-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2424e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2424e-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2424e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2424e-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2424e-148">INPUTS</span></span>

### <span data-ttu-id="2424e-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2424e-149">None</span></span>
<span data-ttu-id="2424e-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2424e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2424e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2424e-151">OUTPUTS</span></span>

## <span data-ttu-id="2424e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2424e-152">NOTES</span></span>

## <span data-ttu-id="2424e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2424e-153">RELATED LINKS</span></span>

[<span data-ttu-id="2424e-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2424e-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2424e-155">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2424e-155">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="2424e-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2424e-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
