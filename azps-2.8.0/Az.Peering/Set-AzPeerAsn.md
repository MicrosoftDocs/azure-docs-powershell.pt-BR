---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772840"
---
# <span data-ttu-id="fb43d-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fb43d-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="fb43d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb43d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb43d-103">Atualizar informações de contato</span><span class="sxs-lookup"><span data-stu-id="fb43d-103">Update Contact Information</span></span>

## <span data-ttu-id="fb43d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb43d-104">SYNTAX</span></span>

### <span data-ttu-id="fb43d-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb43d-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb43d-106">Assume</span><span class="sxs-lookup"><span data-stu-id="fb43d-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb43d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb43d-107">DESCRIPTION</span></span>
<span data-ttu-id="fb43d-108">Permite que você atualize as informações de contato de um PeerAsn na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb43d-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="fb43d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb43d-109">EXAMPLES</span></span>

### <span data-ttu-id="fb43d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb43d-110">Example 1</span></span>
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

<span data-ttu-id="fb43d-111">Adiciona um endereço de e-mail à rede ASN do par</span><span class="sxs-lookup"><span data-stu-id="fb43d-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="fb43d-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb43d-112">PARAMETERS</span></span>

### <span data-ttu-id="fb43d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb43d-113">-AsJob</span></span>
<span data-ttu-id="fb43d-114">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fb43d-114">Run in the background.</span></span>

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

### <span data-ttu-id="fb43d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb43d-115">-DefaultProfile</span></span>
<span data-ttu-id="fb43d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb43d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb43d-117">-Email</span><span class="sxs-lookup"><span data-stu-id="fb43d-117">-Email</span></span>
<span data-ttu-id="fb43d-118">Email</span><span class="sxs-lookup"><span data-stu-id="fb43d-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb43d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb43d-119">-InputObject</span></span>
<span data-ttu-id="fb43d-120">{{Fillobject descrição da entrada}}</span><span class="sxs-lookup"><span data-stu-id="fb43d-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb43d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb43d-121">-Name</span></span>
<span data-ttu-id="fb43d-122">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="fb43d-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb43d-123">-Telefone</span><span class="sxs-lookup"><span data-stu-id="fb43d-123">-Phone</span></span>
<span data-ttu-id="fb43d-124">Telefone</span><span class="sxs-lookup"><span data-stu-id="fb43d-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb43d-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb43d-125">-Confirm</span></span>
<span data-ttu-id="fb43d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb43d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb43d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb43d-127">-WhatIf</span></span>
<span data-ttu-id="fb43d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb43d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb43d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb43d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb43d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb43d-130">CommonParameters</span></span>
<span data-ttu-id="fb43d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb43d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb43d-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb43d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb43d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb43d-133">INPUTS</span></span>

### <span data-ttu-id="fb43d-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fb43d-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="fb43d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb43d-135">OUTPUTS</span></span>

### <span data-ttu-id="fb43d-136">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="fb43d-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="fb43d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb43d-137">NOTES</span></span>

## <span data-ttu-id="fb43d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb43d-138">RELATED LINKS</span></span>
