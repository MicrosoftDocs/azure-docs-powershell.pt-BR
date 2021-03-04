---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889710"
---
# <span data-ttu-id="bc2bc-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="bc2bc-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="bc2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2bc-103">Criar um objeto na memória para ForestTrust</span><span class="sxs-lookup"><span data-stu-id="bc2bc-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="bc2bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc2bc-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="bc2bc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2bc-106">Criar um objeto na memória para ForestTrust</span><span class="sxs-lookup"><span data-stu-id="bc2bc-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="bc2bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="bc2bc-108">Exemplo 1: Criar ServiceForestTrust para ADDomain</span><span class="sxs-lookup"><span data-stu-id="bc2bc-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="bc2bc-109">Criar ServiceForestTrust para ADDomain</span><span class="sxs-lookup"><span data-stu-id="bc2bc-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="bc2bc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-110">PARAMETERS</span></span>

### <span data-ttu-id="bc2bc-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bc2bc-111">-FriendlyName</span></span>
<span data-ttu-id="bc2bc-112">Nome Amigável.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-112">Friendly Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2bc-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="bc2bc-113">-RemoteDnsIP</span></span>
<span data-ttu-id="bc2bc-114">IPs dns remotos.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-114">Remote Dns ips.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2bc-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="bc2bc-115">-TrustDirection</span></span>
<span data-ttu-id="bc2bc-116">Direção de confiança.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-116">Trust Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2bc-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="bc2bc-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="bc2bc-118">FQDN de domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-118">Trusted Domain FQDN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2bc-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="bc2bc-119">-TrustPassword</span></span>
<span data-ttu-id="bc2bc-120">Confiança senha.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2bc-121">CommonParameters</span></span>
<span data-ttu-id="bc2bc-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc2bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2bc-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc2bc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2bc-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-124">INPUTS</span></span>

## <span data-ttu-id="bc2bc-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-125">OUTPUTS</span></span>

### <span data-ttu-id="bc2bc-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="bc2bc-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="bc2bc-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc2bc-127">NOTES</span></span>

<span data-ttu-id="bc2bc-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bc2bc-128">ALIASES</span></span>

## <span data-ttu-id="bc2bc-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc2bc-129">RELATED LINKS</span></span>

