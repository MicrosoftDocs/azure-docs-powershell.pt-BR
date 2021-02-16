---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117792"
---
# <span data-ttu-id="b5ffa-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="b5ffa-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="b5ffa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ffa-103">Criar um novo Objeto de Localização do CosmosDB(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="b5ffa-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b5ffa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5ffa-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5ffa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5ffa-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ffa-106">Criar um novo Objeto de Localização do CosmosDB(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="b5ffa-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b5ffa-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5ffa-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ffa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5ffa-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="b5ffa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5ffa-109">PARAMETERS</span></span>

### <span data-ttu-id="b5ffa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ffa-110">-DefaultProfile</span></span>
<span data-ttu-id="b5ffa-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ffa-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ffa-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="b5ffa-112">-FailoverPriority</span></span>
<span data-ttu-id="b5ffa-113">Prioridade de failover do local.</span><span class="sxs-lookup"><span data-stu-id="b5ffa-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="b5ffa-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b5ffa-114">-IsZoneRedundant</span></span>
<span data-ttu-id="b5ffa-115">Booliana para indicar se essa região é ou não um Zona de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="b5ffa-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="b5ffa-116">-Nomeda Localização</span><span class="sxs-lookup"><span data-stu-id="b5ffa-116">-LocationName</span></span>
<span data-ttu-id="b5ffa-117">Nome do Local na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b5ffa-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="b5ffa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ffa-118">CommonParameters</span></span>
<span data-ttu-id="b5ffa-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ffa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ffa-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5ffa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ffa-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5ffa-121">INPUTS</span></span>

### <span data-ttu-id="b5ffa-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b5ffa-122">None</span></span>

## <span data-ttu-id="b5ffa-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5ffa-123">OUTPUTS</span></span>

### <span data-ttu-id="b5ffa-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="b5ffa-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="b5ffa-125">Notas</span><span class="sxs-lookup"><span data-stu-id="b5ffa-125">NOTES</span></span>

## <span data-ttu-id="b5ffa-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5ffa-126">RELATED LINKS</span></span>
