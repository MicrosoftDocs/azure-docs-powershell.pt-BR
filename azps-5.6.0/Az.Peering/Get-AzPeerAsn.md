---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 9498183e66a0991f7a724065bb5a88e954cd6594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890180"
---
# <span data-ttu-id="04da3-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="04da3-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="04da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04da3-102">SYNOPSIS</span></span>
<span data-ttu-id="04da3-103">Obtém o objeto PeerAsn ARM.</span><span class="sxs-lookup"><span data-stu-id="04da3-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="04da3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04da3-104">SYNTAX</span></span>

### <span data-ttu-id="04da3-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04da3-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04da3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04da3-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04da3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04da3-107">DESCRIPTION</span></span>
<span data-ttu-id="04da3-108">Obtém o PeerAsn para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="04da3-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="04da3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04da3-109">EXAMPLES</span></span>

### <span data-ttu-id="04da3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04da3-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="04da3-111">Obtém o PeerAsn</span><span class="sxs-lookup"><span data-stu-id="04da3-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="04da3-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04da3-112">PARAMETERS</span></span>

### <span data-ttu-id="04da3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04da3-113">-DefaultProfile</span></span>
<span data-ttu-id="04da3-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04da3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04da3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="04da3-115">-Name</span></span>
<span data-ttu-id="04da3-116">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="04da3-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04da3-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04da3-117">-ResourceId</span></span>
<span data-ttu-id="04da3-118">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="04da3-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04da3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04da3-119">CommonParameters</span></span>
<span data-ttu-id="04da3-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04da3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04da3-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04da3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04da3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04da3-122">INPUTS</span></span>

### <span data-ttu-id="04da3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="04da3-123">System.String</span></span>

## <span data-ttu-id="04da3-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04da3-124">OUTPUTS</span></span>

### <span data-ttu-id="04da3-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="04da3-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="04da3-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="04da3-126">NOTES</span></span>

## <span data-ttu-id="04da3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04da3-127">RELATED LINKS</span></span>
