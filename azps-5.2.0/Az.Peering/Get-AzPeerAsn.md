---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259966"
---
# <span data-ttu-id="897e0-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="897e0-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="897e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="897e0-102">SYNOPSIS</span></span>
<span data-ttu-id="897e0-103">Obtém o objeto PeerAsn do ARM.</span><span class="sxs-lookup"><span data-stu-id="897e0-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="897e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="897e0-104">SYNTAX</span></span>

### <span data-ttu-id="897e0-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="897e0-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="897e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="897e0-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="897e0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="897e0-107">DESCRIPTION</span></span>
<span data-ttu-id="897e0-108">Obtém a PeerAsn de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="897e0-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="897e0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="897e0-109">EXAMPLES</span></span>

### <span data-ttu-id="897e0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="897e0-110">Example 1</span></span>
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

<span data-ttu-id="897e0-111">Obtém o PeerAsn</span><span class="sxs-lookup"><span data-stu-id="897e0-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="897e0-112">OS</span><span class="sxs-lookup"><span data-stu-id="897e0-112">PARAMETERS</span></span>

### <span data-ttu-id="897e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897e0-113">-DefaultProfile</span></span>
<span data-ttu-id="897e0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="897e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897e0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="897e0-115">-Name</span></span>
<span data-ttu-id="897e0-116">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="897e0-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="897e0-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="897e0-117">-ResourceId</span></span>
<span data-ttu-id="897e0-118">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="897e0-118">The resource id string name.</span></span>

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

### <span data-ttu-id="897e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897e0-119">CommonParameters</span></span>
<span data-ttu-id="897e0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897e0-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="897e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897e0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="897e0-122">INPUTS</span></span>

### <span data-ttu-id="897e0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="897e0-123">System.String</span></span>

## <span data-ttu-id="897e0-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="897e0-124">OUTPUTS</span></span>

### <span data-ttu-id="897e0-125">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="897e0-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="897e0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="897e0-126">NOTES</span></span>

## <span data-ttu-id="897e0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="897e0-127">RELATED LINKS</span></span>
