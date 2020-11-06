---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchService.md
ms.openlocfilehash: 934ba85d438178ee636d5042f1fa145e63d60291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429355"
---
# <span data-ttu-id="b2790-101">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="b2790-101">New-AzureRmSearchService</span></span>

## <span data-ttu-id="b2790-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2790-102">SYNOPSIS</span></span>
<span data-ttu-id="b2790-103">Cria um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2790-103">Creates an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2790-104">SYNTAX</span></span>

```
New-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2790-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2790-105">DESCRIPTION</span></span>
<span data-ttu-id="b2790-106">O cmdlet **New-AzureRmSearchService** cria um serviço de pesquisa do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="b2790-106">The **New-AzureRmSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="b2790-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2790-107">EXAMPLES</span></span>

### <span data-ttu-id="b2790-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2790-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


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

<span data-ttu-id="b2790-109">O comando cria um serviço de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2790-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="b2790-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2790-110">PARAMETERS</span></span>

### <span data-ttu-id="b2790-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2790-111">-DefaultProfile</span></span>
<span data-ttu-id="b2790-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2790-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2790-113">-Hostingmode</span><span class="sxs-lookup"><span data-stu-id="b2790-113">-HostingMode</span></span>
<span data-ttu-id="b2790-114">Modo de hospedagem do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="b2790-115">-Local</span><span class="sxs-lookup"><span data-stu-id="b2790-115">-Location</span></span>
<span data-ttu-id="b2790-116">Localização do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-116">Search Service location.</span></span>

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

### <span data-ttu-id="b2790-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2790-117">-Name</span></span>
<span data-ttu-id="b2790-118">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-118">Search Service name.</span></span>

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

### <span data-ttu-id="b2790-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b2790-119">-PartitionCount</span></span>
<span data-ttu-id="b2790-120">Contagem da partição do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="b2790-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b2790-121">-ReplicaCount</span></span>
<span data-ttu-id="b2790-122">Contagem de réplica do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="b2790-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2790-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2790-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2790-124">Resource Group name.</span></span>

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

### <span data-ttu-id="b2790-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="b2790-125">-Sku</span></span>
<span data-ttu-id="b2790-126">SKU do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2790-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="b2790-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2790-127">-Confirm</span></span>
<span data-ttu-id="b2790-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2790-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2790-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2790-129">-WhatIf</span></span>
<span data-ttu-id="b2790-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2790-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2790-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2790-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2790-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2790-132">CommonParameters</span></span>
<span data-ttu-id="b2790-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2790-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2790-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2790-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2790-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2790-135">INPUTS</span></span>

### <span data-ttu-id="b2790-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b2790-136">None</span></span>

## <span data-ttu-id="b2790-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2790-137">OUTPUTS</span></span>

### <span data-ttu-id="b2790-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b2790-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b2790-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2790-139">NOTES</span></span>

## <span data-ttu-id="b2790-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2790-140">RELATED LINKS</span></span>

[<span data-ttu-id="b2790-141">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="b2790-141">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="b2790-142">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="b2790-142">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="b2790-143">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="b2790-143">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
