---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: e5f961b5bd3acc1db716d68f43147e1a6c5611f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890178"
---
# <span data-ttu-id="d1c68-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="d1c68-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="d1c68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1c68-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c68-103">Lista as rotas recebidas para um Peering.</span><span class="sxs-lookup"><span data-stu-id="d1c68-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="d1c68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d1c68-104">SYNTAX</span></span>

### <span data-ttu-id="d1c68-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1c68-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1c68-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c68-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c68-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d1c68-107">DESCRIPTION</span></span>
<span data-ttu-id="d1c68-108">Lista as rotas recebidas de um Peering</span><span class="sxs-lookup"><span data-stu-id="d1c68-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="d1c68-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1c68-109">EXAMPLES</span></span>

### <span data-ttu-id="d1c68-110">Listar as 100 principais rotas recebidas para um par</span><span class="sxs-lookup"><span data-stu-id="d1c68-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="d1c68-111">Lista todas as rotas recebidas para um paring</span><span class="sxs-lookup"><span data-stu-id="d1c68-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="d1c68-112">Filtrar por caminho AS</span><span class="sxs-lookup"><span data-stu-id="d1c68-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="d1c68-113">Lista todas as rotas recebidas para um paring com um filtro em AS</span><span class="sxs-lookup"><span data-stu-id="d1c68-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="d1c68-114">Filtrar por RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="d1c68-115">Lista todas as rotas recebidas para um paring com um filtro em RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="d1c68-116">Filtrar por OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="d1c68-117">Lista todas as rotas recebidas para um paring com um filtro em OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="d1c68-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d1c68-118">PARAMETERS</span></span>

### <span data-ttu-id="d1c68-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="d1c68-119">-AsPath</span></span>
<span data-ttu-id="d1c68-120">Filtrar por Caminho AS.</span><span class="sxs-lookup"><span data-stu-id="d1c68-120">Filter by AS Path.</span></span>
<span data-ttu-id="d1c68-121">Exemplo: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="d1c68-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="d1c68-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c68-122">-DefaultProfile</span></span>
<span data-ttu-id="d1c68-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c68-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c68-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d1c68-124">-Name</span></span>
<span data-ttu-id="d1c68-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d1c68-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c68-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-126">-OriginAsValidationState</span></span>
<span data-ttu-id="d1c68-127">Filtrar por origem estado de validação as.</span><span class="sxs-lookup"><span data-stu-id="d1c68-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="d1c68-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d1c68-128">-Prefix</span></span>
<span data-ttu-id="d1c68-129">Filtrar por prefixo.</span><span class="sxs-lookup"><span data-stu-id="d1c68-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="d1c68-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c68-130">-ResourceGroupName</span></span>
<span data-ttu-id="d1c68-131">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d1c68-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="d1c68-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c68-132">-ResourceId</span></span>
<span data-ttu-id="d1c68-133">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="d1c68-133">The resource id string name.</span></span>

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

### <span data-ttu-id="d1c68-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="d1c68-134">-RPKIValidationState</span></span>
<span data-ttu-id="d1c68-135">Filtrar pelo estado de validação RPKI.</span><span class="sxs-lookup"><span data-stu-id="d1c68-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="d1c68-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c68-136">CommonParameters</span></span>
<span data-ttu-id="d1c68-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c68-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c68-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c68-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c68-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1c68-139">INPUTS</span></span>

### <span data-ttu-id="d1c68-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d1c68-140">System.String</span></span>

## <span data-ttu-id="d1c68-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d1c68-141">OUTPUTS</span></span>

### <span data-ttu-id="d1c68-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="d1c68-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="d1c68-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="d1c68-143">NOTES</span></span>

## <span data-ttu-id="d1c68-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1c68-144">RELATED LINKS</span></span>
