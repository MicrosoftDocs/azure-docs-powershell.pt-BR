---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 829bd1f01be1226346d67f9b662915675cd70f80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889789"
---
# <span data-ttu-id="001c2-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="001c2-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="001c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="001c2-102">SYNOPSIS</span></span>
<span data-ttu-id="001c2-103">Crie um novo Objeto de Localização do CosmosDB(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="001c2-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="001c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="001c2-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001c2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="001c2-105">DESCRIPTION</span></span>
<span data-ttu-id="001c2-106">Crie um novo Objeto de Localização do CosmosDB(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="001c2-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="001c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="001c2-107">EXAMPLES</span></span>

### <span data-ttu-id="001c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="001c2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="001c2-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="001c2-109">PARAMETERS</span></span>

### <span data-ttu-id="001c2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001c2-110">-DefaultProfile</span></span>
<span data-ttu-id="001c2-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="001c2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="001c2-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="001c2-112">-FailoverPriority</span></span>
<span data-ttu-id="001c2-113">Prioridade de failover do local.</span><span class="sxs-lookup"><span data-stu-id="001c2-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="001c2-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="001c2-114">-IsZoneRedundant</span></span>
<span data-ttu-id="001c2-115">Boolean para indicar se essa região é ou não um AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="001c2-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="001c2-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="001c2-116">-LocationName</span></span>
<span data-ttu-id="001c2-117">Nome do Local na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="001c2-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="001c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001c2-118">CommonParameters</span></span>
<span data-ttu-id="001c2-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="001c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001c2-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="001c2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001c2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="001c2-121">INPUTS</span></span>

### <span data-ttu-id="001c2-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="001c2-122">None</span></span>

## <span data-ttu-id="001c2-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="001c2-123">OUTPUTS</span></span>

### <span data-ttu-id="001c2-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="001c2-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="001c2-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="001c2-125">NOTES</span></span>

## <span data-ttu-id="001c2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="001c2-126">RELATED LINKS</span></span>
