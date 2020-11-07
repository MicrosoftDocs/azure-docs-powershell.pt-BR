---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944475"
---
# <span data-ttu-id="45d0a-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="45d0a-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="45d0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="45d0a-103">Cria um novo ASN de par</span><span class="sxs-lookup"><span data-stu-id="45d0a-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="45d0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45d0a-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="45d0a-106">Cria um novo objeto PeerAsn para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="45d0a-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="45d0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="45d0a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45d0a-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="45d0a-109">Cria um novo PeerAsn</span><span class="sxs-lookup"><span data-stu-id="45d0a-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="45d0a-110">OS</span><span class="sxs-lookup"><span data-stu-id="45d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="45d0a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45d0a-111">-AsJob</span></span>
<span data-ttu-id="45d0a-112">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="45d0a-112">Run in the background.</span></span>

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

### <span data-ttu-id="45d0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d0a-113">-DefaultProfile</span></span>
<span data-ttu-id="45d0a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45d0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45d0a-115">-Email</span><span class="sxs-lookup"><span data-stu-id="45d0a-115">-Email</span></span>
<span data-ttu-id="45d0a-116">Email</span><span class="sxs-lookup"><span data-stu-id="45d0a-116">Email</span></span>

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

### <span data-ttu-id="45d0a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="45d0a-117">-Name</span></span>
<span data-ttu-id="45d0a-118">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="45d0a-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d0a-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="45d0a-119">-PeerAsn</span></span>
<span data-ttu-id="45d0a-120">A ID do recurso ASN de par. Use Get-AzPeerAsn para recuperar a ID.</span><span class="sxs-lookup"><span data-stu-id="45d0a-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d0a-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="45d0a-121">-PeerName</span></span>
<span data-ttu-id="45d0a-122">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="45d0a-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d0a-123">-Telefone</span><span class="sxs-lookup"><span data-stu-id="45d0a-123">-Phone</span></span>
<span data-ttu-id="45d0a-124">Telefone</span><span class="sxs-lookup"><span data-stu-id="45d0a-124">Phone</span></span>

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

### <span data-ttu-id="45d0a-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45d0a-125">-Confirm</span></span>
<span data-ttu-id="45d0a-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d0a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d0a-127">-WhatIf</span></span>
<span data-ttu-id="45d0a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45d0a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45d0a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45d0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d0a-130">CommonParameters</span></span>
<span data-ttu-id="45d0a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d0a-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45d0a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d0a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45d0a-133">INPUTS</span></span>

### <span data-ttu-id="45d0a-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45d0a-134">None</span></span>

## <span data-ttu-id="45d0a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45d0a-135">OUTPUTS</span></span>

### <span data-ttu-id="45d0a-136">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="45d0a-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="45d0a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45d0a-137">NOTES</span></span>

## <span data-ttu-id="45d0a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45d0a-138">RELATED LINKS</span></span>
