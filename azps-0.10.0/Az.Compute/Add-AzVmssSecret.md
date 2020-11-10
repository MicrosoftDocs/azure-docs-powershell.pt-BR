---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 908810f658cdd4083bd24356eaab4e52d4dd5158
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395111"
---
# <span data-ttu-id="0fbbc-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0fbbc-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="0fbbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbbc-103">Adiciona um segredo a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="0fbbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fbbc-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fbbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbbc-106">O cmdlet **Add-AzVmssSecret** adiciona um segredo ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0fbbc-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0fbbc-107">O segredo deve ser armazenado em um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="0fbbc-108">Para obter mais informações sobre o Key Vault, consulte [o que é o cofre de chave do Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="0fbbc-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="0fbbc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="0fbbc-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="0fbbc-110">Para obter mais informações sobre os cmdlets, consulte [cmdlets do compartimento de chave do Azure](/powershell/module/az.keyvault) ou o cmdlet [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="0fbbc-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="0fbbc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fbbc-111">EXAMPLES</span></span>

### <span data-ttu-id="0fbbc-112">Exemplo 1: adicionar um segredo à VMSS</span><span class="sxs-lookup"><span data-stu-id="0fbbc-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="0fbbc-113">Este exemplo adiciona um segredo à VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="0fbbc-114">O primeiro comando usa o cmdlet Get-AzKeyVault para obter um segredo de cofre do cofre chamado ContosoVault e armazena o resultado na variável chamada $Vault.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="0fbbc-115">O segundo comando usa o cmdlet **New-AzVmssVaultCertificateConfig** para criar uma configuração de certificado de cofre de chaves usando a URL do certificado especificado do repositório de certificados chamado certificados e armazena os resultados na variável chamada $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="0fbbc-116">O terceiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="0fbbc-117">O quarto comando adiciona um segredo ao VMSS usando o segredo do cofre usando a ID do recurso chave e o certificado do cofre armazenado nas variáveis $Vault e $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="0fbbc-118">OS</span><span class="sxs-lookup"><span data-stu-id="0fbbc-118">PARAMETERS</span></span>

### <span data-ttu-id="0fbbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbbc-119">-DefaultProfile</span></span>
<span data-ttu-id="0fbbc-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbbc-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0fbbc-121">-SourceVaultId</span></span>
<span data-ttu-id="0fbbc-122">Especifica a ID do recurso do cofre de chaves que contém os certificados que você pode adicionar à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="0fbbc-123">Esse valor também funciona como a chave para adicionar vários certificados.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="0fbbc-124">Isso significa que você pode usar o mesmo valor para o parâmetro *SourceVaultId* ao adicionar vários certificados do mesmo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="0fbbc-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0fbbc-125">-VaultCertificate</span></span>
<span data-ttu-id="0fbbc-126">Especifica o objeto de **certificado** do cofre que contém a URL do certificado e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="0fbbc-127">Você pode usar o cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="0fbbc-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fbbc-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0fbbc-129">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="0fbbc-130">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="0fbbc-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fbbc-131">-Confirm</span></span>
<span data-ttu-id="0fbbc-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbbc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbbc-133">-WhatIf</span></span>
<span data-ttu-id="0fbbc-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fbbc-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbbc-136">CommonParameters</span></span>
<span data-ttu-id="0fbbc-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbbc-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbbc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbbc-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fbbc-139">INPUTS</span></span>

### <span data-ttu-id="0fbbc-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0fbbc-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="0fbbc-141">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0fbbc-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="0fbbc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fbbc-142">OUTPUTS</span></span>

### <span data-ttu-id="0fbbc-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0fbbc-143">None</span></span>
<span data-ttu-id="0fbbc-144">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0fbbc-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0fbbc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fbbc-145">NOTES</span></span>

## <span data-ttu-id="0fbbc-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fbbc-146">RELATED LINKS</span></span>

[<span data-ttu-id="0fbbc-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="0fbbc-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="0fbbc-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0fbbc-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
