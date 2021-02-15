---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112729"
---
# <span data-ttu-id="87d66-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="87d66-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="87d66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87d66-102">SYNOPSIS</span></span>
<span data-ttu-id="87d66-103">Lista as rotas recebidas para um Peering.</span><span class="sxs-lookup"><span data-stu-id="87d66-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="87d66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87d66-104">SYNTAX</span></span>

### <span data-ttu-id="87d66-105">ByResourceGroupAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87d66-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87d66-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87d66-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87d66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87d66-107">DESCRIPTION</span></span>
<span data-ttu-id="87d66-108">Listas de rotas recebidas de um Peering</span><span class="sxs-lookup"><span data-stu-id="87d66-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="87d66-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87d66-109">EXAMPLES</span></span>

### <span data-ttu-id="87d66-110">Listar as 100 principais rotas recebidas para um peering</span><span class="sxs-lookup"><span data-stu-id="87d66-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="87d66-111">Lista todas as rotas recebidas para um peering</span><span class="sxs-lookup"><span data-stu-id="87d66-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="87d66-112">Filtrar por caminho AS</span><span class="sxs-lookup"><span data-stu-id="87d66-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="87d66-113">Lista todas as rotas recebidas para um peering com um filtro em AS</span><span class="sxs-lookup"><span data-stu-id="87d66-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="87d66-114">Filtrar por LTDKIValidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="87d66-115">Lista todas as rotas recebidas para um peering com um filtro emEIQUIVALidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="87d66-116">Filtrar por OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="87d66-117">Lista todas as rotas recebidas para um peering com um filtro no OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="87d66-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87d66-118">PARAMETERS</span></span>

### <span data-ttu-id="87d66-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="87d66-119">-AsPath</span></span>
<span data-ttu-id="87d66-120">Filtrar por CAMINHO AS.</span><span class="sxs-lookup"><span data-stu-id="87d66-120">Filter by AS Path.</span></span>
<span data-ttu-id="87d66-121">Exemplo: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="87d66-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="87d66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d66-122">-DefaultProfile</span></span>
<span data-ttu-id="87d66-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87d66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d66-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="87d66-124">-Name</span></span>
<span data-ttu-id="87d66-125">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="87d66-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="87d66-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-126">-OriginAsValidationState</span></span>
<span data-ttu-id="87d66-127">Filtrar por estado de validação AS de origem.</span><span class="sxs-lookup"><span data-stu-id="87d66-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="87d66-128">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="87d66-128">-Prefix</span></span>
<span data-ttu-id="87d66-129">Filtrar por prefixo.</span><span class="sxs-lookup"><span data-stu-id="87d66-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="87d66-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d66-130">-ResourceGroupName</span></span>
<span data-ttu-id="87d66-131">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="87d66-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="87d66-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87d66-132">-ResourceId</span></span>
<span data-ttu-id="87d66-133">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="87d66-133">The resource id string name.</span></span>

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

### <span data-ttu-id="87d66-134">-EIKIValidationState</span><span class="sxs-lookup"><span data-stu-id="87d66-134">-RPKIValidationState</span></span>
<span data-ttu-id="87d66-135">Filtrar por estado de validação DE ACORDOKI.</span><span class="sxs-lookup"><span data-stu-id="87d66-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="87d66-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d66-136">CommonParameters</span></span>
<span data-ttu-id="87d66-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d66-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d66-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87d66-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d66-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="87d66-139">INPUTS</span></span>

### <span data-ttu-id="87d66-140">System.String</span><span class="sxs-lookup"><span data-stu-id="87d66-140">System.String</span></span>

## <span data-ttu-id="87d66-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="87d66-141">OUTPUTS</span></span>

### <span data-ttu-id="87d66-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReshellRoute</span><span class="sxs-lookup"><span data-stu-id="87d66-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="87d66-143">Notas</span><span class="sxs-lookup"><span data-stu-id="87d66-143">NOTES</span></span>

## <span data-ttu-id="87d66-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87d66-144">RELATED LINKS</span></span>
