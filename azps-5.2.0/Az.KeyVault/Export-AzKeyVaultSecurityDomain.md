---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264451"
---
# <span data-ttu-id="da661-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="da661-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="da661-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da661-102">SYNOPSIS</span></span>
<span data-ttu-id="da661-103">Exporta os dados do domínio de segurança de um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="da661-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="da661-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da661-104">SYNTAX</span></span>

### <span data-ttu-id="da661-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="da661-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da661-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="da661-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da661-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da661-107">DESCRIPTION</span></span>
<span data-ttu-id="da661-108">Exporta os dados do domínio de segurança de um HSM gerenciado para importação em outro HSM.</span><span class="sxs-lookup"><span data-stu-id="da661-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="da661-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da661-109">EXAMPLES</span></span>

### <span data-ttu-id="da661-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da661-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="da661-111">Esse comando recupera o HSM gerenciado chamado testmhsm e salva um backup desse domínio de segurança do HSM gerenciado para o arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="da661-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="da661-112">OS</span><span class="sxs-lookup"><span data-stu-id="da661-112">PARAMETERS</span></span>

### <span data-ttu-id="da661-113">-Certificados</span><span class="sxs-lookup"><span data-stu-id="da661-113">-Certificates</span></span>
<span data-ttu-id="da661-114">Caminhos para os certificados que são usados para criptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="da661-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="da661-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da661-115">-DefaultProfile</span></span>
<span data-ttu-id="da661-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da661-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da661-117">-Force</span><span class="sxs-lookup"><span data-stu-id="da661-117">-Force</span></span>
<span data-ttu-id="da661-118">Especifique se deseja substituir o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="da661-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="da661-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da661-119">-InputObject</span></span>
<span data-ttu-id="da661-120">Objeto que representa um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="da661-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="da661-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="da661-121">-Name</span></span>
<span data-ttu-id="da661-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="da661-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="da661-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="da661-123">-OutputPath</span></span>
<span data-ttu-id="da661-124">Especifique o caminho onde os dados do domínio de segurança serão baixados.</span><span class="sxs-lookup"><span data-stu-id="da661-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="da661-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da661-125">-PassThru</span></span>
<span data-ttu-id="da661-126">Quando especificado, um booliano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="da661-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="da661-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="da661-127">-Quorum</span></span>
<span data-ttu-id="da661-128">O número mínimo de partilhas necessários para descriptografar o domínio de segurança para recuperação.</span><span class="sxs-lookup"><span data-stu-id="da661-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="da661-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da661-129">-Confirm</span></span>
<span data-ttu-id="da661-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da661-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da661-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da661-131">-WhatIf</span></span>
<span data-ttu-id="da661-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da661-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da661-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da661-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da661-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da661-134">CommonParameters</span></span>
<span data-ttu-id="da661-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da661-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da661-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da661-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da661-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da661-137">INPUTS</span></span>

### <span data-ttu-id="da661-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="da661-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="da661-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da661-139">OUTPUTS</span></span>

### <span data-ttu-id="da661-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da661-140">System.Boolean</span></span>

## <span data-ttu-id="da661-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da661-141">NOTES</span></span>

## <span data-ttu-id="da661-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da661-142">RELATED LINKS</span></span>
