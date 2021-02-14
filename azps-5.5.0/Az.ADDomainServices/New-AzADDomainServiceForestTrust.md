---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110866"
---
# <span data-ttu-id="4a769-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="4a769-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="4a769-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a769-102">SYNOPSIS</span></span>
<span data-ttu-id="4a769-103">Criar um objeto na memória para ForestTrust</span><span class="sxs-lookup"><span data-stu-id="4a769-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="4a769-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a769-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="4a769-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a769-105">DESCRIPTION</span></span>
<span data-ttu-id="4a769-106">Criar um objeto na memória para ForestTrust</span><span class="sxs-lookup"><span data-stu-id="4a769-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="4a769-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a769-107">EXAMPLES</span></span>

### <span data-ttu-id="4a769-108">Exemplo 1: Criar ServiceForestTrust para ADDomain</span><span class="sxs-lookup"><span data-stu-id="4a769-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="4a769-109">Criar ServiceForestTrust para ADDomain</span><span class="sxs-lookup"><span data-stu-id="4a769-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="4a769-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a769-110">PARAMETERS</span></span>

### <span data-ttu-id="4a769-111">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="4a769-111">-FriendlyName</span></span>
<span data-ttu-id="4a769-112">Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="4a769-112">Friendly Name.</span></span>

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

### <span data-ttu-id="4a769-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="4a769-113">-RemoteDnsIP</span></span>
<span data-ttu-id="4a769-114">IPs dns remotos.</span><span class="sxs-lookup"><span data-stu-id="4a769-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="4a769-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="4a769-115">-TrustDirection</span></span>
<span data-ttu-id="4a769-116">Direção da Confiança.</span><span class="sxs-lookup"><span data-stu-id="4a769-116">Trust Direction.</span></span>

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

### <span data-ttu-id="4a769-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="4a769-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="4a769-118">FQDN de domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="4a769-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="4a769-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="4a769-119">-TrustPassword</span></span>
<span data-ttu-id="4a769-120">Confiar na Senha.</span><span class="sxs-lookup"><span data-stu-id="4a769-120">Trust Password.</span></span>

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

### <span data-ttu-id="4a769-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a769-121">CommonParameters</span></span>
<span data-ttu-id="4a769-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a769-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a769-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a769-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a769-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="4a769-124">INPUTS</span></span>

## <span data-ttu-id="4a769-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="4a769-125">OUTPUTS</span></span>

### <span data-ttu-id="4a769-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="4a769-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="4a769-127">Notas</span><span class="sxs-lookup"><span data-stu-id="4a769-127">NOTES</span></span>

<span data-ttu-id="4a769-128">Aliases</span><span class="sxs-lookup"><span data-stu-id="4a769-128">ALIASES</span></span>

## <span data-ttu-id="4a769-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a769-129">RELATED LINKS</span></span>

