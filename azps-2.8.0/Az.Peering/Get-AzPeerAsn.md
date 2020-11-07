---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772864"
---
# <span data-ttu-id="1ab94-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1ab94-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="1ab94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ab94-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab94-103">Obtém o objeto PeerAsn do ARM.</span><span class="sxs-lookup"><span data-stu-id="1ab94-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="1ab94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ab94-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ab94-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ab94-105">DESCRIPTION</span></span>
<span data-ttu-id="1ab94-106">Obtém a PeerAsn de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1ab94-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="1ab94-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ab94-107">EXAMPLES</span></span>

### <span data-ttu-id="1ab94-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ab94-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="1ab94-109">Obtém o PeerAsn</span><span class="sxs-lookup"><span data-stu-id="1ab94-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="1ab94-110">OS</span><span class="sxs-lookup"><span data-stu-id="1ab94-110">PARAMETERS</span></span>

### <span data-ttu-id="1ab94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab94-111">-DefaultProfile</span></span>
<span data-ttu-id="1ab94-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ab94-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ab94-113">-Name</span></span>
<span data-ttu-id="1ab94-114">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="1ab94-114">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1ab94-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab94-115">CommonParameters</span></span>
<span data-ttu-id="1ab94-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab94-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab94-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ab94-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab94-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ab94-118">INPUTS</span></span>

### <span data-ttu-id="1ab94-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ab94-119">None</span></span>

## <span data-ttu-id="1ab94-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ab94-120">OUTPUTS</span></span>

### <span data-ttu-id="1ab94-121">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1ab94-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="1ab94-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ab94-122">NOTES</span></span>

## <span data-ttu-id="1ab94-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ab94-123">RELATED LINKS</span></span>
