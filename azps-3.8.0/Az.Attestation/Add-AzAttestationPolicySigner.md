---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: df46bc097ce4a1a52c486bb0e418bce656f0f476
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942742"
---
# <span data-ttu-id="0e71c-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="0e71c-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="0e71c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e71c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e71c-103">Adiciona um signatário de política confiável para um locatário no Azure atestado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0e71c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e71c-104">SYNTAX</span></span>

### <span data-ttu-id="0e71c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e71c-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e71c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e71c-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e71c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e71c-107">DESCRIPTION</span></span>
<span data-ttu-id="0e71c-108">O cmdlet Add-AzAttestationPolicySigner adiciona um signatário de política confiável para um locatário no Azure atestado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0e71c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e71c-109">EXAMPLES</span></span>

### <span data-ttu-id="0e71c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e71c-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="0e71c-111">Adicione um signatário confiável para o provedor de Atteestation chamado *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="0e71c-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="0e71c-112">OS</span><span class="sxs-lookup"><span data-stu-id="0e71c-112">PARAMETERS</span></span>

### <span data-ttu-id="0e71c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e71c-113">-DefaultProfile</span></span>
<span data-ttu-id="0e71c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e71c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e71c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e71c-115">-Name</span></span>
<span data-ttu-id="0e71c-116">Especifica o nome de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="0e71c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e71c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e71c-118">Especifica o nome do grupo de recursos de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="0e71c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e71c-119">-ResourceId</span></span>
<span data-ttu-id="0e71c-120">Especifica o ResourceId de um provedor de atestado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="0e71c-121">-Signatário</span><span class="sxs-lookup"><span data-stu-id="0e71c-121">-Signer</span></span>
<span data-ttu-id="0e71c-122">Especifica o token da Web RFC7519 JSON que contém uma declaração chamada "AAS-policyCertificate" cujo valor é uma chave JSON RFC7517 da Web que contém uma nova chave de assinatura confiável a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="0e71c-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="0e71c-123">O JWT RFC7519 deve ser assinado com uma das chaves de assinatura confiáveis existentes.</span><span class="sxs-lookup"><span data-stu-id="0e71c-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="0e71c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e71c-124">-Confirm</span></span>
<span data-ttu-id="0e71c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e71c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e71c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e71c-126">-WhatIf</span></span>
<span data-ttu-id="0e71c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e71c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e71c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e71c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e71c-129">CommonParameters</span></span>
<span data-ttu-id="0e71c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e71c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e71c-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e71c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e71c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e71c-132">INPUTS</span></span>

### <span data-ttu-id="0e71c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e71c-133">System.String</span></span>

## <span data-ttu-id="0e71c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e71c-134">OUTPUTS</span></span>

### <span data-ttu-id="0e71c-135">Microsoft. Azure. Commands.. Models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="0e71c-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="0e71c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e71c-136">NOTES</span></span>

## <span data-ttu-id="0e71c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e71c-137">RELATED LINKS</span></span>
