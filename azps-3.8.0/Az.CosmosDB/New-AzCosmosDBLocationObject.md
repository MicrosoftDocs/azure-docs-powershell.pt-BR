---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943646"
---
# <span data-ttu-id="84a46-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="84a46-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="84a46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84a46-102">SYNOPSIS</span></span>
<span data-ttu-id="84a46-103">Crie um novo objeto de localização de CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="84a46-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="84a46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84a46-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84a46-105">DESCRIPTION</span></span>
<span data-ttu-id="84a46-106">Crie um novo objeto de localização de CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="84a46-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="84a46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84a46-107">EXAMPLES</span></span>

### <span data-ttu-id="84a46-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84a46-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="84a46-109">OS</span><span class="sxs-lookup"><span data-stu-id="84a46-109">PARAMETERS</span></span>

### <span data-ttu-id="84a46-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a46-110">-DefaultProfile</span></span>
<span data-ttu-id="84a46-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84a46-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a46-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="84a46-112">-FailoverPriority</span></span>
<span data-ttu-id="84a46-113">Prioridade de failover do local.</span><span class="sxs-lookup"><span data-stu-id="84a46-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="84a46-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="84a46-114">-IsZoneRedundant</span></span>
<span data-ttu-id="84a46-115">Booliano para indicar se essa região é ou não uma AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="84a46-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="84a46-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="84a46-116">-LocationName</span></span>
<span data-ttu-id="84a46-117">Nome do local na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="84a46-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="84a46-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a46-118">CommonParameters</span></span>
<span data-ttu-id="84a46-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a46-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a46-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84a46-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a46-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84a46-121">INPUTS</span></span>

### <span data-ttu-id="84a46-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="84a46-122">None</span></span>

## <span data-ttu-id="84a46-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84a46-123">OUTPUTS</span></span>

### <span data-ttu-id="84a46-124">Microsoft. Azure. Commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="84a46-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="84a46-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84a46-125">NOTES</span></span>

## <span data-ttu-id="84a46-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84a46-126">RELATED LINKS</span></span>
