---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/set-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Set-AzureRmSearchService.md
ms.openlocfilehash: c938dd611d9f6d731c07d5aee76cb390838f4679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429352"
---
# <span data-ttu-id="ae59f-101">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-101">Set-AzureRmSearchService</span></span>

## <span data-ttu-id="ae59f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae59f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae59f-103">Atualizar um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae59f-103">Update an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae59f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae59f-104">SYNTAX</span></span>

### <span data-ttu-id="ae59f-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae59f-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae59f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae59f-106">InputObjectParameterSet</span></span>
```
Set-AzureRmSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae59f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae59f-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae59f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae59f-108">DESCRIPTION</span></span>
<span data-ttu-id="ae59f-109">O cmdlet **set-AzureRmSearchService** modifica um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae59f-109">The **Set-AzureRmSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="ae59f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae59f-110">EXAMPLES</span></span>

### <span data-ttu-id="ae59f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae59f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


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

<span data-ttu-id="ae59f-112">O exemplo altera a contagem de partições e a contagem de réplicas do serviço de pesquisa do Azure para 2.</span><span class="sxs-lookup"><span data-stu-id="ae59f-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="ae59f-113">OS</span><span class="sxs-lookup"><span data-stu-id="ae59f-113">PARAMETERS</span></span>

### <span data-ttu-id="ae59f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae59f-114">-DefaultProfile</span></span>
<span data-ttu-id="ae59f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae59f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae59f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae59f-116">-InputObject</span></span>
<span data-ttu-id="ae59f-117">Objeto de entrada do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae59f-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="ae59f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae59f-118">-Name</span></span>
<span data-ttu-id="ae59f-119">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae59f-119">Search Service name.</span></span>

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

### <span data-ttu-id="ae59f-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="ae59f-120">-PartitionCount</span></span>
<span data-ttu-id="ae59f-121">Contagem da partição do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae59f-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="ae59f-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ae59f-122">-ReplicaCount</span></span>
<span data-ttu-id="ae59f-123">Contagem de réplica do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae59f-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="ae59f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae59f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae59f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae59f-125">Resource Group name.</span></span>

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

### <span data-ttu-id="ae59f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae59f-126">-ResourceId</span></span>
<span data-ttu-id="ae59f-127">ID do recurso do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ae59f-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="ae59f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae59f-128">-Confirm</span></span>
<span data-ttu-id="ae59f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae59f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae59f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae59f-130">-WhatIf</span></span>
<span data-ttu-id="ae59f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae59f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae59f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae59f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae59f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae59f-133">CommonParameters</span></span>
<span data-ttu-id="ae59f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae59f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae59f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae59f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae59f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae59f-136">INPUTS</span></span>

### <span data-ttu-id="ae59f-137">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="ae59f-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae59f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ae59f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ae59f-139">System.String</span></span>

## <span data-ttu-id="ae59f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae59f-140">OUTPUTS</span></span>

### <span data-ttu-id="ae59f-141">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="ae59f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae59f-142">NOTES</span></span>

## <span data-ttu-id="ae59f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae59f-143">RELATED LINKS</span></span>

[<span data-ttu-id="ae59f-144">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-144">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="ae59f-145">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-145">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="ae59f-146">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ae59f-146">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
