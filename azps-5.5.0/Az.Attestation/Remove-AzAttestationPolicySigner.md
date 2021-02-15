---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112267"
---
# <span data-ttu-id="c1810-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="c1810-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="c1810-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1810-102">SYNOPSIS</span></span>
<span data-ttu-id="c1810-103">Remove um signatário de política confiável para um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="c1810-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c1810-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1810-104">SYNTAX</span></span>

### <span data-ttu-id="c1810-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1810-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1810-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1810-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1810-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1810-107">DESCRIPTION</span></span>
<span data-ttu-id="c1810-108">O Remove-AzAttestationPolicySigner cmdlet remove um signatário de política confiável para um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="c1810-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c1810-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1810-109">EXAMPLES</span></span>

### <span data-ttu-id="c1810-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1810-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="c1810-111">Remover um signator confiável para o Provedor de Teste chamado *pshtest.*</span><span class="sxs-lookup"><span data-stu-id="c1810-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="c1810-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1810-112">PARAMETERS</span></span>

### <span data-ttu-id="c1810-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1810-113">-DefaultProfile</span></span>
<span data-ttu-id="c1810-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1810-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1810-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1810-115">-Name</span></span>
<span data-ttu-id="c1810-116">Especifica o nome de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="c1810-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1810-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1810-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1810-118">Especifica o nome do grupo de recursos de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="c1810-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1810-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1810-119">-ResourceId</span></span>
<span data-ttu-id="c1810-120">Especifica a ResourceID de um provedor de teste.</span><span class="sxs-lookup"><span data-stu-id="c1810-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1810-121">-Signator</span><span class="sxs-lookup"><span data-stu-id="c1810-121">-Signer</span></span>
<span data-ttu-id="c1810-122">Especifica o RFC7519 JSON Web Token contendo uma reivindicação chamada "maa-policyCertificate" cujo valor é uma Chave Web JSON JSON RFC7517 que contém uma chave de assinatura confiável a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c1810-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="c1810-123">A RFC7519 JWT deve ser assinada com uma das chaves de assinatura confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="c1810-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="c1810-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1810-124">-Confirm</span></span>
<span data-ttu-id="c1810-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1810-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1810-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1810-126">-WhatIf</span></span>
<span data-ttu-id="c1810-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1810-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1810-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1810-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1810-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1810-129">CommonParameters</span></span>
<span data-ttu-id="c1810-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1810-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1810-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1810-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1810-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1810-132">INPUTS</span></span>

### <span data-ttu-id="c1810-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c1810-133">System.String</span></span>

## <span data-ttu-id="c1810-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1810-134">OUTPUTS</span></span>

### <span data-ttu-id="c1810-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="c1810-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="c1810-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c1810-136">NOTES</span></span>

## <span data-ttu-id="c1810-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1810-137">RELATED LINKS</span></span>
