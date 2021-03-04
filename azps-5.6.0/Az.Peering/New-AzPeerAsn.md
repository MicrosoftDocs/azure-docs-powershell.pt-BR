---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 11f3a729c6818a7794a8b42a4b21a658530cc60d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890159"
---
# <span data-ttu-id="752bf-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="752bf-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="752bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752bf-102">SYNOPSIS</span></span>
<span data-ttu-id="752bf-103">Cria um novo ASN par</span><span class="sxs-lookup"><span data-stu-id="752bf-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="752bf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="752bf-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="752bf-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="752bf-105">DESCRIPTION</span></span>
<span data-ttu-id="752bf-106">Cria um novo objeto PeerAsn para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="752bf-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="752bf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="752bf-107">EXAMPLES</span></span>

### <span data-ttu-id="752bf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="752bf-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="752bf-109">Cria um novo PeerAsn</span><span class="sxs-lookup"><span data-stu-id="752bf-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="752bf-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="752bf-110">PARAMETERS</span></span>

### <span data-ttu-id="752bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="752bf-111">-AsJob</span></span>
<span data-ttu-id="752bf-112">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="752bf-112">Run in the background.</span></span>

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

### <span data-ttu-id="752bf-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="752bf-113">-ContactDetail</span></span>
<span data-ttu-id="752bf-114">Endereços de email usados para entrar em contato se problemas normalmente arrise um Centro de Operações de Rede</span><span class="sxs-lookup"><span data-stu-id="752bf-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752bf-115">-DefaultProfile</span></span>
<span data-ttu-id="752bf-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="752bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="752bf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="752bf-117">-Name</span></span>
<span data-ttu-id="752bf-118">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="752bf-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="752bf-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="752bf-119">-PeerAsn</span></span>
<span data-ttu-id="752bf-120">A ID de Recurso de Asn Par. Use Get-AzPeerAsn recuperar a Id.</span><span class="sxs-lookup"><span data-stu-id="752bf-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="752bf-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="752bf-121">-PeerName</span></span>
<span data-ttu-id="752bf-122">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="752bf-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="752bf-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="752bf-123">-Confirm</span></span>
<span data-ttu-id="752bf-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="752bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752bf-125">-WhatIf</span></span>
<span data-ttu-id="752bf-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="752bf-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="752bf-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="752bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752bf-128">CommonParameters</span></span>
<span data-ttu-id="752bf-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752bf-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="752bf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752bf-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="752bf-131">INPUTS</span></span>

### <span data-ttu-id="752bf-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="752bf-132">None</span></span>

## <span data-ttu-id="752bf-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="752bf-133">OUTPUTS</span></span>

### <span data-ttu-id="752bf-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="752bf-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="752bf-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="752bf-135">NOTES</span></span>

## <span data-ttu-id="752bf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="752bf-136">RELATED LINKS</span></span>
