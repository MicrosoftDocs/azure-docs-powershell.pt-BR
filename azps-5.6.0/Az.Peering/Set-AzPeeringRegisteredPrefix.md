---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 2990b28e811b21940d51ce8d0fd9c7540feccfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890121"
---
# <span data-ttu-id="aed3d-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="aed3d-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="aed3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed3d-102">SYNOPSIS</span></span>
<span data-ttu-id="aed3d-103">Define ou atualiza um prefixo registrado do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="aed3d-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="aed3d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aed3d-104">SYNTAX</span></span>

### <span data-ttu-id="aed3d-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aed3d-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aed3d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="aed3d-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aed3d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aed3d-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed3d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aed3d-108">DESCRIPTION</span></span>
<span data-ttu-id="aed3d-109">Permite a atualização de um prefixo registrado do recurso de paração pai.</span><span class="sxs-lookup"><span data-stu-id="aed3d-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="aed3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aed3d-110">EXAMPLES</span></span>

### <span data-ttu-id="aed3d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aed3d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="aed3d-112">Atualiza o prefixo por id de recurso.</span><span class="sxs-lookup"><span data-stu-id="aed3d-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="aed3d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aed3d-113">PARAMETERS</span></span>

### <span data-ttu-id="aed3d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aed3d-114">-AsJob</span></span>
<span data-ttu-id="aed3d-115">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="aed3d-115">Run in the background.</span></span>

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

### <span data-ttu-id="aed3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed3d-116">-DefaultProfile</span></span>
<span data-ttu-id="aed3d-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aed3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aed3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aed3d-118">-InputObject</span></span>
<span data-ttu-id="aed3d-119">Usar um Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="aed3d-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aed3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aed3d-120">-Name</span></span>
<span data-ttu-id="aed3d-121">O nome do prefixo.</span><span class="sxs-lookup"><span data-stu-id="aed3d-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed3d-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="aed3d-122">-PeeringName</span></span>
<span data-ttu-id="aed3d-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="aed3d-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed3d-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="aed3d-124">-Prefix</span></span>
<span data-ttu-id="aed3d-125">O prefixo IPv4 da sessão</span><span class="sxs-lookup"><span data-stu-id="aed3d-125">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed3d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed3d-126">-ResourceGroupName</span></span>
<span data-ttu-id="aed3d-127">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="aed3d-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed3d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aed3d-128">-ResourceId</span></span>
<span data-ttu-id="aed3d-129">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="aed3d-129">The resource id string name.</span></span>

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

### <span data-ttu-id="aed3d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aed3d-130">-Confirm</span></span>
<span data-ttu-id="aed3d-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aed3d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed3d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed3d-132">-WhatIf</span></span>
<span data-ttu-id="aed3d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aed3d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed3d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aed3d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed3d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed3d-135">CommonParameters</span></span>
<span data-ttu-id="aed3d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed3d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed3d-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aed3d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed3d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aed3d-138">INPUTS</span></span>

### <span data-ttu-id="aed3d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="aed3d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="aed3d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aed3d-140">System.String</span></span>

## <span data-ttu-id="aed3d-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aed3d-141">OUTPUTS</span></span>

### <span data-ttu-id="aed3d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="aed3d-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="aed3d-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="aed3d-143">NOTES</span></span>

## <span data-ttu-id="aed3d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aed3d-144">RELATED LINKS</span></span>
