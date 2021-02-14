---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e5d65cb334070cdc5e861a2f90bd95277d41fab5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110808"
---
# <span data-ttu-id="b3a9f-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b3a9f-101">Get-AzSearchService</span></span>

## <span data-ttu-id="b3a9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a9f-103">Obtém um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b3a9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3a9f-104">SYNTAX</span></span>

### <span data-ttu-id="b3a9f-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3a9f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a9f-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a9f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3a9f-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a9f-108">O **cmdlet Get-AzSearchService** obtém o serviço especificado de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="b3a9f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3a9f-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a9f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3a9f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="b3a9f-111">Obter um serviço de Pesquisa Cognitiva do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="b3a9f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3a9f-112">PARAMETERS</span></span>

### <span data-ttu-id="b3a9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a9f-113">-DefaultProfile</span></span>
<span data-ttu-id="b3a9f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a9f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3a9f-115">-Name</span></span>
<span data-ttu-id="b3a9f-116">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-116">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3a9f-118">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a9f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a9f-119">-ResourceId</span></span>
<span data-ttu-id="b3a9f-120">ID do Recurso do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b3a9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a9f-121">CommonParameters</span></span>
<span data-ttu-id="b3a9f-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a9f-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a9f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a9f-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="b3a9f-124">INPUTS</span></span>

### <span data-ttu-id="b3a9f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b3a9f-125">System.String</span></span>

## <span data-ttu-id="b3a9f-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="b3a9f-126">OUTPUTS</span></span>

### <span data-ttu-id="b3a9f-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b3a9f-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b3a9f-128">Notas</span><span class="sxs-lookup"><span data-stu-id="b3a9f-128">NOTES</span></span>

## <span data-ttu-id="b3a9f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3a9f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b3a9f-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b3a9f-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="b3a9f-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b3a9f-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="b3a9f-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b3a9f-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)