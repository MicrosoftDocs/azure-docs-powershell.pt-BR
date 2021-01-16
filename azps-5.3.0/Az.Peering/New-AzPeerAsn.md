---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272553"
---
# <span data-ttu-id="b1154-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b1154-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="b1154-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1154-102">SYNOPSIS</span></span>
<span data-ttu-id="b1154-103">Cria um novo ASN de par</span><span class="sxs-lookup"><span data-stu-id="b1154-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="b1154-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1154-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1154-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1154-105">DESCRIPTION</span></span>
<span data-ttu-id="b1154-106">Cria um novo objeto PeerAsn para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b1154-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="b1154-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1154-107">EXAMPLES</span></span>

### <span data-ttu-id="b1154-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1154-108">Example 1</span></span>
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

<span data-ttu-id="b1154-109">Cria um novo PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b1154-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="b1154-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1154-110">PARAMETERS</span></span>

### <span data-ttu-id="b1154-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1154-111">-AsJob</span></span>
<span data-ttu-id="b1154-112">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b1154-112">Run in the background.</span></span>

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

### <span data-ttu-id="b1154-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="b1154-113">-ContactDetail</span></span>
<span data-ttu-id="b1154-114">Endereços de email usados para entrar em contato se os problemas arrise normalmente um centro de operações de rede</span><span class="sxs-lookup"><span data-stu-id="b1154-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="b1154-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1154-115">-DefaultProfile</span></span>
<span data-ttu-id="b1154-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1154-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1154-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1154-117">-Name</span></span>
<span data-ttu-id="b1154-118">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b1154-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b1154-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="b1154-119">-PeerAsn</span></span>
<span data-ttu-id="b1154-120">A ID do recurso ASN de par. Use Get-AzPeerAsn para recuperar a ID.</span><span class="sxs-lookup"><span data-stu-id="b1154-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="b1154-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="b1154-121">-PeerName</span></span>
<span data-ttu-id="b1154-122">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b1154-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b1154-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1154-123">-Confirm</span></span>
<span data-ttu-id="b1154-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1154-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1154-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1154-125">-WhatIf</span></span>
<span data-ttu-id="b1154-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1154-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1154-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1154-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1154-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1154-128">CommonParameters</span></span>
<span data-ttu-id="b1154-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1154-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1154-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1154-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1154-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1154-131">INPUTS</span></span>

### <span data-ttu-id="b1154-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1154-132">None</span></span>

## <span data-ttu-id="b1154-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1154-133">OUTPUTS</span></span>

### <span data-ttu-id="b1154-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b1154-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="b1154-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1154-135">NOTES</span></span>

## <span data-ttu-id="b1154-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1154-136">RELATED LINKS</span></span>
