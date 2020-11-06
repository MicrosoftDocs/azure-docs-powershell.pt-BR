---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 5967ffbb5b0a39a771604c2f456de008d98de5fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599269"
---
# <span data-ttu-id="245f4-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-101">Set-AzSearchService</span></span>

## <span data-ttu-id="245f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="245f4-102">SYNOPSIS</span></span>
<span data-ttu-id="245f4-103">Atualizar um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="245f4-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="245f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="245f4-104">SYNTAX</span></span>

### <span data-ttu-id="245f4-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="245f4-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="245f4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="245f4-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="245f4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="245f4-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="245f4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="245f4-108">DESCRIPTION</span></span>
<span data-ttu-id="245f4-109">O cmdlet **set-AzSearchService** modifica um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="245f4-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="245f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="245f4-110">EXAMPLES</span></span>

### <span data-ttu-id="245f4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="245f4-111">Example 1</span></span>
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

<span data-ttu-id="245f4-112">O exemplo altera a contagem de partições e a contagem de réplicas do serviço de pesquisa do Azure para 2.</span><span class="sxs-lookup"><span data-stu-id="245f4-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="245f4-113">OS</span><span class="sxs-lookup"><span data-stu-id="245f4-113">PARAMETERS</span></span>

### <span data-ttu-id="245f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245f4-114">-DefaultProfile</span></span>
<span data-ttu-id="245f4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="245f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="245f4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="245f4-116">-InputObject</span></span>
<span data-ttu-id="245f4-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="245f4-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="245f4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="245f4-118">-Name</span></span>
<span data-ttu-id="245f4-119">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="245f4-119">Search Service name.</span></span>

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

### <span data-ttu-id="245f4-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="245f4-120">-PartitionCount</span></span>
<span data-ttu-id="245f4-121">Contagem da partição do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="245f4-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="245f4-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="245f4-122">-ReplicaCount</span></span>
<span data-ttu-id="245f4-123">Contagem de réplica do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="245f4-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="245f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="245f4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="245f4-125">Resource Group name.</span></span>

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

### <span data-ttu-id="245f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="245f4-126">-ResourceId</span></span>
<span data-ttu-id="245f4-127">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="245f4-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="245f4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="245f4-128">-Confirm</span></span>
<span data-ttu-id="245f4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245f4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="245f4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245f4-130">-WhatIf</span></span>
<span data-ttu-id="245f4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="245f4-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="245f4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="245f4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="245f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245f4-133">CommonParameters</span></span>
<span data-ttu-id="245f4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245f4-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245f4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245f4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="245f4-136">INPUTS</span></span>

### <span data-ttu-id="245f4-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="245f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="245f4-138">System.String</span></span>

## <span data-ttu-id="245f4-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="245f4-139">OUTPUTS</span></span>

### <span data-ttu-id="245f4-140">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="245f4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="245f4-141">NOTES</span></span>

## <span data-ttu-id="245f4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="245f4-142">RELATED LINKS</span></span>

[<span data-ttu-id="245f4-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="245f4-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="245f4-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="245f4-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)