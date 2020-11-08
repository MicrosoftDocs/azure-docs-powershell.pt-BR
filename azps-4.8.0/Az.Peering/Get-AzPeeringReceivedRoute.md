---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114299"
---
# <span data-ttu-id="132e0-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="132e0-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="132e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="132e0-102">SYNOPSIS</span></span>
<span data-ttu-id="132e0-103">Lista as rotas recebidas para um emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="132e0-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="132e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="132e0-104">SYNTAX</span></span>

### <span data-ttu-id="132e0-105">ByResourceGroupAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="132e0-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="132e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="132e0-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="132e0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="132e0-107">DESCRIPTION</span></span>
<span data-ttu-id="132e0-108">Lista as rotas recebidas de um emparelhamento</span><span class="sxs-lookup"><span data-stu-id="132e0-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="132e0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="132e0-109">EXAMPLES</span></span>

### <span data-ttu-id="132e0-110">Lista superior 100 de rotas recebidas para um emparelhamento</span><span class="sxs-lookup"><span data-stu-id="132e0-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="132e0-111">Lista todas as rotas recebidas para um emparelhamento</span><span class="sxs-lookup"><span data-stu-id="132e0-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="132e0-112">Filtrar por como caminho</span><span class="sxs-lookup"><span data-stu-id="132e0-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="132e0-113">Lista todas as rotas recebidas para um emparelhamento com um filtro ativado como</span><span class="sxs-lookup"><span data-stu-id="132e0-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="132e0-114">Filtrar por RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="132e0-115">Lista todas as rotas recebidas para um emparelhamento com um filtro em RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="132e0-116">Filtrar por OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="132e0-117">Lista todas as rotas recebidas para um emparelhamento com um filtro em OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="132e0-118">OS</span><span class="sxs-lookup"><span data-stu-id="132e0-118">PARAMETERS</span></span>

### <span data-ttu-id="132e0-119">-ASPATH</span><span class="sxs-lookup"><span data-stu-id="132e0-119">-AsPath</span></span>
<span data-ttu-id="132e0-120">Filtrar por como caminho.</span><span class="sxs-lookup"><span data-stu-id="132e0-120">Filter by AS Path.</span></span>
<span data-ttu-id="132e0-121">Exemplo: ' 9342 1234 4567 '</span><span class="sxs-lookup"><span data-stu-id="132e0-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="132e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132e0-122">-DefaultProfile</span></span>
<span data-ttu-id="132e0-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="132e0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132e0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="132e0-124">-Name</span></span>
<span data-ttu-id="132e0-125">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="132e0-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="132e0-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-126">-OriginAsValidationState</span></span>
<span data-ttu-id="132e0-127">Filtrar por origem como estado de validação.</span><span class="sxs-lookup"><span data-stu-id="132e0-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="132e0-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="132e0-128">-Prefix</span></span>
<span data-ttu-id="132e0-129">Filtrar por prefixo.</span><span class="sxs-lookup"><span data-stu-id="132e0-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="132e0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="132e0-130">-ResourceGroupName</span></span>
<span data-ttu-id="132e0-131">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="132e0-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="132e0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="132e0-132">-ResourceId</span></span>
<span data-ttu-id="132e0-133">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="132e0-133">The resource id string name.</span></span>

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

### <span data-ttu-id="132e0-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="132e0-134">-RPKIValidationState</span></span>
<span data-ttu-id="132e0-135">Filtrar por RPKI estado de validação.</span><span class="sxs-lookup"><span data-stu-id="132e0-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="132e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132e0-136">CommonParameters</span></span>
<span data-ttu-id="132e0-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132e0-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="132e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132e0-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="132e0-139">INPUTS</span></span>

### <span data-ttu-id="132e0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="132e0-140">System.String</span></span>

## <span data-ttu-id="132e0-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="132e0-141">OUTPUTS</span></span>

### <span data-ttu-id="132e0-142">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="132e0-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="132e0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="132e0-143">NOTES</span></span>

## <span data-ttu-id="132e0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="132e0-144">RELATED LINKS</span></span>
