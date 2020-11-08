---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114722"
---
# <span data-ttu-id="e18cf-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e18cf-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="e18cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e18cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e18cf-103">Remover ASN par</span><span class="sxs-lookup"><span data-stu-id="e18cf-103">Remove Peer Asn</span></span>

## <span data-ttu-id="e18cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e18cf-104">SYNTAX</span></span>

### <span data-ttu-id="e18cf-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e18cf-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18cf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e18cf-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18cf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e18cf-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18cf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e18cf-108">DESCRIPTION</span></span>
<span data-ttu-id="e18cf-109">Remova um PeerAsn da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e18cf-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="e18cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e18cf-110">EXAMPLES</span></span>

### <span data-ttu-id="e18cf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e18cf-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="e18cf-112">Remove o peer ASN</span><span class="sxs-lookup"><span data-stu-id="e18cf-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="e18cf-113">OS</span><span class="sxs-lookup"><span data-stu-id="e18cf-113">PARAMETERS</span></span>

### <span data-ttu-id="e18cf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e18cf-114">-AsJob</span></span>
<span data-ttu-id="e18cf-115">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e18cf-115">Run in the background.</span></span>

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

### <span data-ttu-id="e18cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18cf-116">-DefaultProfile</span></span>
<span data-ttu-id="e18cf-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e18cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e18cf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e18cf-118">-Force</span></span>
<span data-ttu-id="e18cf-119">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e18cf-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="e18cf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e18cf-120">-InputObject</span></span>
<span data-ttu-id="e18cf-121">O objeto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="e18cf-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e18cf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e18cf-122">-Name</span></span>
<span data-ttu-id="e18cf-123">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e18cf-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18cf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e18cf-124">-PassThru</span></span>
<span data-ttu-id="e18cf-125">Retornar true se concluir</span><span class="sxs-lookup"><span data-stu-id="e18cf-125">Return true if complete</span></span>

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

### <span data-ttu-id="e18cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e18cf-126">-ResourceId</span></span>
<span data-ttu-id="e18cf-127">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e18cf-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18cf-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e18cf-128">-Confirm</span></span>
<span data-ttu-id="e18cf-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e18cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18cf-130">-WhatIf</span></span>
<span data-ttu-id="e18cf-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e18cf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e18cf-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e18cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e18cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18cf-133">CommonParameters</span></span>
<span data-ttu-id="e18cf-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18cf-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e18cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18cf-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e18cf-136">INPUTS</span></span>

### <span data-ttu-id="e18cf-137">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e18cf-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="e18cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e18cf-138">System.String</span></span>

## <span data-ttu-id="e18cf-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e18cf-139">OUTPUTS</span></span>

### <span data-ttu-id="e18cf-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e18cf-140">System.Boolean</span></span>

## <span data-ttu-id="e18cf-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e18cf-141">NOTES</span></span>

## <span data-ttu-id="e18cf-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e18cf-142">RELATED LINKS</span></span>
