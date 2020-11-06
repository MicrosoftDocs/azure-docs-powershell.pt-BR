---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602036"
---
# <span data-ttu-id="52e98-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="52e98-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="52e98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52e98-102">SYNOPSIS</span></span>
<span data-ttu-id="52e98-103">Adiciona um segredo a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="52e98-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52e98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52e98-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e98-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52e98-105">DESCRIPTION</span></span>
<span data-ttu-id="52e98-106">O cmdlet **Add-AzureRmVmssSecret** adiciona um segredo ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="52e98-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="52e98-107">O segredo deve ser armazenado em um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="52e98-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="52e98-108">Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chave do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="52e98-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="52e98-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="52e98-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="52e98-110">Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) na biblioteca Microsoft Developer Network ou cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="52e98-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="52e98-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52e98-111">EXAMPLES</span></span>

### <span data-ttu-id="52e98-112">Exemplo 1: adicionar um segredo à VMSS</span><span class="sxs-lookup"><span data-stu-id="52e98-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="52e98-113">Este exemplo adiciona um segredo à VMSS.</span><span class="sxs-lookup"><span data-stu-id="52e98-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="52e98-114">O primeiro comando usa o cmdlet Get-AzureRmKeyVault para obter um segredo de cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.</span><span class="sxs-lookup"><span data-stu-id="52e98-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="52e98-115">O segundo comando usa o cmdlet **New-AzureRmVmssVaultCertificateConfig** para criar uma configuração de certificado de cofre de chaves usando a URL do certificado especificado do repositório de certificados chamado certificados e armazena os resultados na variável chamada $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="52e98-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="52e98-116">O terceiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="52e98-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="52e98-117">O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID do recurso chave e o certificado do cofre armazenado nas variáveis $Vault e $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="52e98-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="52e98-118">OS</span><span class="sxs-lookup"><span data-stu-id="52e98-118">PARAMETERS</span></span>

### <span data-ttu-id="52e98-119">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="52e98-119">-SourceVaultId</span></span>
<span data-ttu-id="52e98-120">Especifica a ID do recurso do cofre de chaves que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52e98-120">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="52e98-121">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="52e98-121">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="52e98-122">Isso significa que você pode usar o mesmo valor para o parâmetro *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="52e98-122">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="52e98-123">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="52e98-123">-VaultCertificate</span></span>
<span data-ttu-id="52e98-124">Especifica o objeto de **certificado** do cofre que contém a URL do certificado e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="52e98-124">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="52e98-125">Você pode usar o cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="52e98-125">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="52e98-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52e98-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="52e98-127">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="52e98-127">Specifies the VMSS object.</span></span>
<span data-ttu-id="52e98-128">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="52e98-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52e98-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52e98-129">-Confirm</span></span>
<span data-ttu-id="52e98-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52e98-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e98-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e98-131">-WhatIf</span></span>
<span data-ttu-id="52e98-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52e98-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52e98-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52e98-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e98-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e98-134">CommonParameters</span></span>
<span data-ttu-id="52e98-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e98-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e98-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52e98-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e98-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52e98-137">INPUTS</span></span>

### <span data-ttu-id="52e98-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="52e98-138">None</span></span>
<span data-ttu-id="52e98-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="52e98-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52e98-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52e98-140">OUTPUTS</span></span>

###  
<span data-ttu-id="52e98-141">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="52e98-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="52e98-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52e98-142">NOTES</span></span>

## <span data-ttu-id="52e98-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52e98-143">RELATED LINKS</span></span>

[<span data-ttu-id="52e98-144">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="52e98-144">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="52e98-145">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="52e98-145">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
