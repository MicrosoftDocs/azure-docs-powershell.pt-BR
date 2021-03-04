---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: d4f04c47c37446b6521c122b7551263809bb1c49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887915"
---
# <span data-ttu-id="ada0e-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="ada0e-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="ada0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada0e-102">SYNOPSIS</span></span>
<span data-ttu-id="ada0e-103">Adiciona um signatário de política confiável para um locatário no Atestado do Azure.</span><span class="sxs-lookup"><span data-stu-id="ada0e-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ada0e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ada0e-104">SYNTAX</span></span>

### <span data-ttu-id="ada0e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada0e-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ada0e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada0e-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada0e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ada0e-107">DESCRIPTION</span></span>
<span data-ttu-id="ada0e-108">O Add-AzAttestationPolicySigner cmdlet adiciona um signatário de política confiável para um locatário no Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="ada0e-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ada0e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ada0e-109">EXAMPLES</span></span>

### <span data-ttu-id="ada0e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ada0e-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="ada0e-111">Adicione um signante confiável para o Provedor de Atteestation chamado *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="ada0e-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="ada0e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ada0e-112">PARAMETERS</span></span>

### <span data-ttu-id="ada0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada0e-113">-DefaultProfile</span></span>
<span data-ttu-id="ada0e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ada0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada0e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ada0e-115">-Name</span></span>
<span data-ttu-id="ada0e-116">Especifica o nome de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="ada0e-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="ada0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ada0e-118">Especifica o nome do grupo de recursos de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="ada0e-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="ada0e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ada0e-119">-ResourceId</span></span>
<span data-ttu-id="ada0e-120">Especifica o ResourceID de um provedor de atestados.</span><span class="sxs-lookup"><span data-stu-id="ada0e-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="ada0e-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="ada0e-121">-Signer</span></span>
<span data-ttu-id="ada0e-122">Especifica o Token Web JSON JSON RFC7519 contendo uma declaração chamada "maa-policyCertificate" cujo valor é uma Chave Web JSON JSON RFC7517 que contém uma nova chave de assinatura confiável para adicionar.</span><span class="sxs-lookup"><span data-stu-id="ada0e-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="ada0e-123">A JWT RFC7519 deve ser assinada com uma das chaves de assinatura confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="ada0e-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="ada0e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ada0e-124">-Confirm</span></span>
<span data-ttu-id="ada0e-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada0e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada0e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada0e-126">-WhatIf</span></span>
<span data-ttu-id="ada0e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ada0e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada0e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ada0e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada0e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada0e-129">CommonParameters</span></span>
<span data-ttu-id="ada0e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada0e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada0e-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ada0e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada0e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ada0e-132">INPUTS</span></span>

### <span data-ttu-id="ada0e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ada0e-133">System.String</span></span>

## <span data-ttu-id="ada0e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ada0e-134">OUTPUTS</span></span>

### <span data-ttu-id="ada0e-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="ada0e-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="ada0e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ada0e-136">NOTES</span></span>

## <span data-ttu-id="ada0e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ada0e-137">RELATED LINKS</span></span>
