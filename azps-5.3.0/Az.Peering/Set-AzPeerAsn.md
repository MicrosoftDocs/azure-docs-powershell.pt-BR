---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272525"
---
# <span data-ttu-id="a3819-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3819-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="a3819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3819-102">SYNOPSIS</span></span>
<span data-ttu-id="a3819-103">Atualizar informações de contato</span><span class="sxs-lookup"><span data-stu-id="a3819-103">Update Contact Information</span></span>

## <span data-ttu-id="a3819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3819-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3819-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3819-105">DESCRIPTION</span></span>
<span data-ttu-id="a3819-106">Permite que você atualize as informações de contato de um PeerAsn na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a3819-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="a3819-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3819-107">EXAMPLES</span></span>

### <span data-ttu-id="a3819-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3819-108">Example 1</span></span>
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

<span data-ttu-id="a3819-109">Adiciona um endereço de e-mail à rede ASN do par</span><span class="sxs-lookup"><span data-stu-id="a3819-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="a3819-110">OS</span><span class="sxs-lookup"><span data-stu-id="a3819-110">PARAMETERS</span></span>

### <span data-ttu-id="a3819-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3819-111">-AsJob</span></span>
<span data-ttu-id="a3819-112">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a3819-112">Run in the background.</span></span>

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

### <span data-ttu-id="a3819-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3819-113">-DefaultProfile</span></span>
<span data-ttu-id="a3819-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3819-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3819-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3819-115">-InputObject</span></span>
<span data-ttu-id="a3819-116">{{Fillobject descrição da entrada}}</span><span class="sxs-lookup"><span data-stu-id="a3819-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="a3819-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3819-117">-Confirm</span></span>
<span data-ttu-id="a3819-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3819-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3819-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3819-119">-WhatIf</span></span>
<span data-ttu-id="a3819-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3819-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3819-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3819-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3819-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3819-122">CommonParameters</span></span>
<span data-ttu-id="a3819-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3819-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3819-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3819-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3819-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3819-125">INPUTS</span></span>

### <span data-ttu-id="a3819-126">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3819-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a3819-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3819-127">OUTPUTS</span></span>

### <span data-ttu-id="a3819-128">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3819-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a3819-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3819-129">NOTES</span></span>

## <span data-ttu-id="a3819-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3819-130">RELATED LINKS</span></span>
