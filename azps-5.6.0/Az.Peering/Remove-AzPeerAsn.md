---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890140"
---
# <span data-ttu-id="450ef-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="450ef-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="450ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="450ef-102">SYNOPSIS</span></span>
<span data-ttu-id="450ef-103">Remover a asn de par</span><span class="sxs-lookup"><span data-stu-id="450ef-103">Remove Peer Asn</span></span>

## <span data-ttu-id="450ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="450ef-104">SYNTAX</span></span>

### <span data-ttu-id="450ef-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="450ef-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450ef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="450ef-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450ef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="450ef-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450ef-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="450ef-108">DESCRIPTION</span></span>
<span data-ttu-id="450ef-109">Remova um PeerAsn da assinatura.</span><span class="sxs-lookup"><span data-stu-id="450ef-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="450ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="450ef-110">EXAMPLES</span></span>

### <span data-ttu-id="450ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="450ef-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="450ef-112">Remove o Peer Asn</span><span class="sxs-lookup"><span data-stu-id="450ef-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="450ef-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="450ef-113">PARAMETERS</span></span>

### <span data-ttu-id="450ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="450ef-114">-AsJob</span></span>
<span data-ttu-id="450ef-115">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="450ef-115">Run in the background.</span></span>

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

### <span data-ttu-id="450ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450ef-116">-DefaultProfile</span></span>
<span data-ttu-id="450ef-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="450ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450ef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="450ef-118">-Force</span></span>
<span data-ttu-id="450ef-119">{{ Descrição da Força de Preenchimento }}</span><span class="sxs-lookup"><span data-stu-id="450ef-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="450ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450ef-120">-InputObject</span></span>
<span data-ttu-id="450ef-121">O objeto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="450ef-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="450ef-122">-Name</span><span class="sxs-lookup"><span data-stu-id="450ef-122">-Name</span></span>
<span data-ttu-id="450ef-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="450ef-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="450ef-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="450ef-124">-PassThru</span></span>
<span data-ttu-id="450ef-125">Retornar true se concluído</span><span class="sxs-lookup"><span data-stu-id="450ef-125">Return true if complete</span></span>

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

### <span data-ttu-id="450ef-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="450ef-126">-ResourceId</span></span>
<span data-ttu-id="450ef-127">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="450ef-127">The resource id string name.</span></span>

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

### <span data-ttu-id="450ef-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="450ef-128">-Confirm</span></span>
<span data-ttu-id="450ef-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="450ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450ef-130">-WhatIf</span></span>
<span data-ttu-id="450ef-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="450ef-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="450ef-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="450ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450ef-133">CommonParameters</span></span>
<span data-ttu-id="450ef-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450ef-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="450ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450ef-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="450ef-136">INPUTS</span></span>

### <span data-ttu-id="450ef-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="450ef-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="450ef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="450ef-138">System.String</span></span>

## <span data-ttu-id="450ef-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="450ef-139">OUTPUTS</span></span>

### <span data-ttu-id="450ef-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="450ef-140">System.Boolean</span></span>

## <span data-ttu-id="450ef-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="450ef-141">NOTES</span></span>

## <span data-ttu-id="450ef-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="450ef-142">RELATED LINKS</span></span>
