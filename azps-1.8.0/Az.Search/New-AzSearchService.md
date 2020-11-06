---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 67c5ccb24267825313612cc539f243551ad1894e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599274"
---
# <span data-ttu-id="db114-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="db114-101">New-AzSearchService</span></span>

## <span data-ttu-id="db114-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db114-102">SYNOPSIS</span></span>
<span data-ttu-id="db114-103">Cria um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="db114-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="db114-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db114-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db114-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db114-105">DESCRIPTION</span></span>
<span data-ttu-id="db114-106">O cmdlet **New-AzSearchService** cria um serviço de pesquisa do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="db114-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="db114-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db114-107">EXAMPLES</span></span>

### <span data-ttu-id="db114-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db114-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="db114-109">O comando cria um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="db114-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="db114-110">OS</span><span class="sxs-lookup"><span data-stu-id="db114-110">PARAMETERS</span></span>

### <span data-ttu-id="db114-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db114-111">-DefaultProfile</span></span>
<span data-ttu-id="db114-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db114-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db114-113">-Hostingmode</span><span class="sxs-lookup"><span data-stu-id="db114-113">-HostingMode</span></span>
<span data-ttu-id="db114-114">Modo de hospedagem do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db114-115">-Local</span><span class="sxs-lookup"><span data-stu-id="db114-115">-Location</span></span>
<span data-ttu-id="db114-116">Localização do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db114-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="db114-117">-Name</span></span>
<span data-ttu-id="db114-118">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db114-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="db114-119">-PartitionCount</span></span>
<span data-ttu-id="db114-120">Contagem da partição do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="db114-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="db114-121">-ReplicaCount</span></span>
<span data-ttu-id="db114-122">Contagem de réplica do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="db114-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db114-123">-ResourceGroupName</span></span>
<span data-ttu-id="db114-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db114-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db114-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="db114-125">-Sku</span></span>
<span data-ttu-id="db114-126">SKU do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="db114-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db114-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db114-127">-Confirm</span></span>
<span data-ttu-id="db114-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db114-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db114-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db114-129">-WhatIf</span></span>
<span data-ttu-id="db114-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db114-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db114-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db114-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db114-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db114-132">CommonParameters</span></span>
<span data-ttu-id="db114-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db114-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db114-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db114-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db114-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db114-135">INPUTS</span></span>

### <span data-ttu-id="db114-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db114-136">None</span></span>

## <span data-ttu-id="db114-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db114-137">OUTPUTS</span></span>

### <span data-ttu-id="db114-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="db114-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="db114-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db114-139">NOTES</span></span>

## <span data-ttu-id="db114-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db114-140">RELATED LINKS</span></span>

[<span data-ttu-id="db114-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="db114-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="db114-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="db114-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="db114-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="db114-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)