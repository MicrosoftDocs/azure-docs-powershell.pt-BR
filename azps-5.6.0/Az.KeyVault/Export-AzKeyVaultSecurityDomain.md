---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 6373ddf37e95c8451afbe8a24b6bade2ca5d3bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890840"
---
# <span data-ttu-id="1f800-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="1f800-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="1f800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f800-102">SYNOPSIS</span></span>
<span data-ttu-id="1f800-103">Exporta os dados de domínio de segurança de um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1f800-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="1f800-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f800-104">SYNTAX</span></span>

### <span data-ttu-id="1f800-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f800-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f800-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f800-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f800-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f800-107">DESCRIPTION</span></span>
<span data-ttu-id="1f800-108">Exporta os dados de domínio de segurança de um HSM gerenciado para importação em outro HSM.</span><span class="sxs-lookup"><span data-stu-id="1f800-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="1f800-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f800-109">EXAMPLES</span></span>

### <span data-ttu-id="1f800-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f800-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="1f800-111">Este comando recupera o HSM gerenciado chamado testmhsm e salva um backup desse domínio de segurança HSM gerenciado no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1f800-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="1f800-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f800-112">PARAMETERS</span></span>

### <span data-ttu-id="1f800-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="1f800-113">-Certificates</span></span>
<span data-ttu-id="1f800-114">Caminhos para os certificados usados para criptografar os dados de domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="1f800-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f800-115">-DefaultProfile</span></span>
<span data-ttu-id="1f800-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f800-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f800-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f800-117">-Force</span></span>
<span data-ttu-id="1f800-118">Especifique se deve substituir o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="1f800-118">Specify whether to overwrite existing file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f800-119">-InputObject</span></span>
<span data-ttu-id="1f800-120">Objeto representando um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1f800-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1f800-121">-Name</span></span>
<span data-ttu-id="1f800-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1f800-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1f800-123">-OutputPath</span></span>
<span data-ttu-id="1f800-124">Especifique o caminho para o qual os dados de domínio de segurança serão baixados.</span><span class="sxs-lookup"><span data-stu-id="1f800-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f800-125">-PassThru</span></span>
<span data-ttu-id="1f800-126">Quando especificado, um booleano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1f800-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="1f800-127">-Quorum</span></span>
<span data-ttu-id="1f800-128">O número mínimo de compartilhamentos necessário para descriptografar o domínio de segurança para recuperação.</span><span class="sxs-lookup"><span data-stu-id="1f800-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f800-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f800-129">-Confirm</span></span>
<span data-ttu-id="1f800-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f800-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f800-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f800-131">-WhatIf</span></span>
<span data-ttu-id="1f800-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f800-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f800-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f800-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f800-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f800-134">CommonParameters</span></span>
<span data-ttu-id="1f800-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f800-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f800-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f800-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f800-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f800-137">INPUTS</span></span>

### <span data-ttu-id="1f800-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1f800-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1f800-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f800-139">OUTPUTS</span></span>

### <span data-ttu-id="1f800-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f800-140">System.Boolean</span></span>

## <span data-ttu-id="1f800-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f800-141">NOTES</span></span>

## <span data-ttu-id="1f800-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f800-142">RELATED LINKS</span></span>
