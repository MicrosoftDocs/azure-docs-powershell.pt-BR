---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: fd4058cd09ad0d0ca27f8324368cd6d0277cec7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890127"
---
# <span data-ttu-id="43890-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="43890-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="43890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43890-102">SYNOPSIS</span></span>
<span data-ttu-id="43890-103">Atualizar Informações de Contato</span><span class="sxs-lookup"><span data-stu-id="43890-103">Update Contact Information</span></span>

## <span data-ttu-id="43890-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="43890-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43890-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="43890-105">DESCRIPTION</span></span>
<span data-ttu-id="43890-106">Permite que você atualize informações de contato para um PeerAsn na assinatura.</span><span class="sxs-lookup"><span data-stu-id="43890-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="43890-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43890-107">EXAMPLES</span></span>

### <span data-ttu-id="43890-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43890-108">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="43890-109">Adiciona um endereço de email ao Peer Asn</span><span class="sxs-lookup"><span data-stu-id="43890-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="43890-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="43890-110">PARAMETERS</span></span>

### <span data-ttu-id="43890-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43890-111">-AsJob</span></span>
<span data-ttu-id="43890-112">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="43890-112">Run in the background.</span></span>

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

### <span data-ttu-id="43890-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43890-113">-DefaultProfile</span></span>
<span data-ttu-id="43890-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43890-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43890-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43890-115">-InputObject</span></span>
<span data-ttu-id="43890-116">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="43890-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43890-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43890-117">-Confirm</span></span>
<span data-ttu-id="43890-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43890-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43890-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43890-119">-WhatIf</span></span>
<span data-ttu-id="43890-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43890-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43890-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43890-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43890-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43890-122">CommonParameters</span></span>
<span data-ttu-id="43890-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43890-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43890-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43890-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43890-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43890-125">INPUTS</span></span>

### <span data-ttu-id="43890-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="43890-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="43890-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="43890-127">OUTPUTS</span></span>

### <span data-ttu-id="43890-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="43890-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="43890-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="43890-129">NOTES</span></span>

## <span data-ttu-id="43890-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43890-130">RELATED LINKS</span></span>
