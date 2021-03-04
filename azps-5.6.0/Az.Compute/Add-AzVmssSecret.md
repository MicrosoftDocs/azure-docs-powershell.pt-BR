---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: ec07964f62a22385d98c8cd9b8c98ea0b088ec8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887577"
---
# <span data-ttu-id="11f4f-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="11f4f-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="11f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="11f4f-103">Adiciona um segredo a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="11f4f-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="11f4f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11f4f-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11f4f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="11f4f-106">O cmdlet **Add-AzVmssSecret** adiciona um segredo ao Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="11f4f-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="11f4f-107">O segredo deve ser armazenado em um Cofre de Chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="11f4f-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="11f4f-108">Para obter mais informações relacionadas ao Cofre de Chaves, consulte [O que é o Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="11f4f-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="11f4f-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="11f4f-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="11f4f-110">Para obter mais informações sobre os cmdlets, consulte [Cmdlets do Azure Key Vault](/powershell/module/az.keyvault) ou o cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="11f4f-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="11f4f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11f4f-111">EXAMPLES</span></span>

### <span data-ttu-id="11f4f-112">Exemplo 1: Adicionar um segredo ao VMSS</span><span class="sxs-lookup"><span data-stu-id="11f4f-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="11f4f-113">Este exemplo adiciona um segredo ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="11f4f-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="11f4f-114">O primeiro comando usa o cmdlet Get-AzKeyVault para obter um segredo de cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.</span><span class="sxs-lookup"><span data-stu-id="11f4f-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="11f4f-115">O segundo comando usa o cmdlet **New-AzVmssVaultCertificateConfig** para criar uma configuração de certificado do Cofre de Chaves usando a URL de certificado especificada do armazenamento de certificados denominado Certificados e armazena os resultados na variável chamada $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="11f4f-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="11f4f-116">O terceiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável denominada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="11f4f-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="11f4f-117">O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID do recurso de chave e o certificado de cofre armazenado nas variáveis $Vault e $CertConfig chave.</span><span class="sxs-lookup"><span data-stu-id="11f4f-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="11f4f-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11f4f-118">PARAMETERS</span></span>

### <span data-ttu-id="11f4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f4f-119">-DefaultProfile</span></span>
<span data-ttu-id="11f4f-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="11f4f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f4f-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="11f4f-121">-SourceVaultId</span></span>
<span data-ttu-id="11f4f-122">Especifica a ID de recurso do Cofre de Chaves que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11f4f-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="11f4f-123">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="11f4f-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="11f4f-124">Isso significa que você pode usar o mesmo valor para o *parâmetro SourceVaultId* quando adicionar vários certificados do mesmo Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="11f4f-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="11f4f-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="11f4f-125">-VaultCertificate</span></span>
<span data-ttu-id="11f4f-126">Especifica o objeto Certificado **do** Cofre que contém a URL do certificado e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="11f4f-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="11f4f-127">Você pode usar o cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="11f4f-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="11f4f-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11f4f-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="11f4f-129">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="11f4f-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="11f4f-130">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="11f4f-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="11f4f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11f4f-131">-Confirm</span></span>
<span data-ttu-id="11f4f-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11f4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11f4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f4f-133">-WhatIf</span></span>
<span data-ttu-id="11f4f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11f4f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11f4f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11f4f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11f4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f4f-136">CommonParameters</span></span>
<span data-ttu-id="11f4f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f4f-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11f4f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f4f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11f4f-139">INPUTS</span></span>

### <span data-ttu-id="11f4f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11f4f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="11f4f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="11f4f-141">System.String</span></span>

### <span data-ttu-id="11f4f-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="11f4f-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="11f4f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11f4f-143">OUTPUTS</span></span>

### <span data-ttu-id="11f4f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11f4f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="11f4f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="11f4f-145">NOTES</span></span>

## <span data-ttu-id="11f4f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11f4f-146">RELATED LINKS</span></span>

[<span data-ttu-id="11f4f-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="11f4f-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="11f4f-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11f4f-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
