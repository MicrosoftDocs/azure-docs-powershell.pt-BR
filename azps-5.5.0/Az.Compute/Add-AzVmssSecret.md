---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117877"
---
# <span data-ttu-id="623a5-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="623a5-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="623a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="623a5-102">SYNOPSIS</span></span>
<span data-ttu-id="623a5-103">Adiciona um segredo a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="623a5-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="623a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="623a5-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="623a5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="623a5-105">DESCRIPTION</span></span>
<span data-ttu-id="623a5-106">O cmdlet **Add-AzVmssSecsec ltd** adiciona um segredo ao VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="623a5-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="623a5-107">O segredo deve ser armazenado em um Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="623a5-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="623a5-108">Para saber mais sobre o Cofre de Teclas, confira [o que é o Cofre de Teclas do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="623a5-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="623a5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="623a5-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="623a5-110">Para obter mais informações sobre os cmdlets, consulte [Cmdlets](/powershell/module/az.keyvault) do Cofre de Tecla do Azure ou o cmdlet [Set-AzKeyVaultSec ltd.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="623a5-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="623a5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="623a5-111">EXAMPLES</span></span>

### <span data-ttu-id="623a5-112">Exemplo 1: Adicionar um segredo ao VMSS</span><span class="sxs-lookup"><span data-stu-id="623a5-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="623a5-113">Este exemplo adiciona um segredo ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="623a5-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="623a5-114">O primeiro comando usa o cmdlet Get-AzKeyVault para obter um segredo do cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.</span><span class="sxs-lookup"><span data-stu-id="623a5-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="623a5-115">O segundo comando usa o cmdlet **New-AzVmsVaultCertificateConfig** para criar uma configuração de certificado do Cofre de Chave usando a URL de certificado especificada do armazenamento de certificados chamado Certificados e armazena os resultados na variável chamada $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="623a5-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="623a5-116">O terceiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="623a5-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="623a5-117">O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID de recurso chave e o certificado do cofre armazenado nas variáveis $Vault e $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="623a5-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="623a5-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="623a5-118">PARAMETERS</span></span>

### <span data-ttu-id="623a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623a5-119">-DefaultProfile</span></span>
<span data-ttu-id="623a5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="623a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623a5-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="623a5-121">-SourceVaultId</span></span>
<span data-ttu-id="623a5-122">Especifica a ID de recurso do Cofre de Teclas que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="623a5-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="623a5-123">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="623a5-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="623a5-124">Isso significa que você pode usar o mesmo valor para o parâmetro *SourceVaultId* ao adicionar vários certificados do mesmo Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="623a5-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="623a5-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="623a5-125">-VaultCertificate</span></span>
<span data-ttu-id="623a5-126">Especifica o objeto Certificado **do** Cofre que contém a URL do certificado e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="623a5-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="623a5-127">Você pode usar o cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="623a5-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="623a5-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="623a5-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="623a5-129">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="623a5-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="623a5-130">Você pode usar [o cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="623a5-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="623a5-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="623a5-131">-Confirm</span></span>
<span data-ttu-id="623a5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="623a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="623a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623a5-133">-WhatIf</span></span>
<span data-ttu-id="623a5-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="623a5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="623a5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="623a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="623a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623a5-136">CommonParameters</span></span>
<span data-ttu-id="623a5-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623a5-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="623a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623a5-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="623a5-139">INPUTS</span></span>

### <span data-ttu-id="623a5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="623a5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="623a5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="623a5-141">System.String</span></span>

### <span data-ttu-id="623a5-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="623a5-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="623a5-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="623a5-143">OUTPUTS</span></span>

### <span data-ttu-id="623a5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="623a5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="623a5-145">Notas</span><span class="sxs-lookup"><span data-stu-id="623a5-145">NOTES</span></span>

## <span data-ttu-id="623a5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="623a5-146">RELATED LINKS</span></span>

[<span data-ttu-id="623a5-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="623a5-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="623a5-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="623a5-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
