---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943483"
---
# <span data-ttu-id="31daa-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-101">Set-AzSearchService</span></span>

## <span data-ttu-id="31daa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31daa-102">SYNOPSIS</span></span>
<span data-ttu-id="31daa-103">Atualizar um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="31daa-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="31daa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31daa-104">SYNTAX</span></span>

### <span data-ttu-id="31daa-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="31daa-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31daa-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31daa-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31daa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31daa-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31daa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31daa-108">DESCRIPTION</span></span>
<span data-ttu-id="31daa-109">O cmdlet **set-AzSearchService** modifica um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="31daa-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="31daa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31daa-110">EXAMPLES</span></span>

### <span data-ttu-id="31daa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31daa-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="31daa-112">O exemplo altera a contagem de partições e a contagem de réplicas do serviço de pesquisa do Azure para 2.</span><span class="sxs-lookup"><span data-stu-id="31daa-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="31daa-113">OS</span><span class="sxs-lookup"><span data-stu-id="31daa-113">PARAMETERS</span></span>

### <span data-ttu-id="31daa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31daa-114">-DefaultProfile</span></span>
<span data-ttu-id="31daa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31daa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31daa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31daa-116">-InputObject</span></span>
<span data-ttu-id="31daa-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="31daa-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="31daa-118">-Name</span></span>
<span data-ttu-id="31daa-119">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="31daa-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="31daa-120">-PartitionCount</span></span>
<span data-ttu-id="31daa-121">Contagem da partição do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="31daa-121">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="31daa-122">-ReplicaCount</span></span>
<span data-ttu-id="31daa-123">Contagem de réplica do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="31daa-123">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31daa-124">-ResourceGroupName</span></span>
<span data-ttu-id="31daa-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31daa-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31daa-126">-ResourceId</span></span>
<span data-ttu-id="31daa-127">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="31daa-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31daa-128">-Confirm</span></span>
<span data-ttu-id="31daa-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31daa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31daa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31daa-130">-WhatIf</span></span>
<span data-ttu-id="31daa-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31daa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31daa-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31daa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31daa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31daa-133">CommonParameters</span></span>
<span data-ttu-id="31daa-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31daa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31daa-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31daa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31daa-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31daa-136">INPUTS</span></span>

### <span data-ttu-id="31daa-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="31daa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="31daa-138">System.String</span></span>

## <span data-ttu-id="31daa-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31daa-139">OUTPUTS</span></span>

### <span data-ttu-id="31daa-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="31daa-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31daa-141">NOTES</span></span>

## <span data-ttu-id="31daa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31daa-142">RELATED LINKS</span></span>

[<span data-ttu-id="31daa-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="31daa-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="31daa-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="31daa-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)