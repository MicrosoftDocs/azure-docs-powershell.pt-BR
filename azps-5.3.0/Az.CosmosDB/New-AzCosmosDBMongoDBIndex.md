---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434055"
---
# <span data-ttu-id="ee8c3-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="ee8c3-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="ee8c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee8c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8c3-103">Cria um novo índice do MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="ee8c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee8c3-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee8c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee8c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8c3-106">O **New-AzCosmosDBMongoDBIndex** cria um novo índice CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="ee8c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee8c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8c3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee8c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="ee8c3-109">OS</span><span class="sxs-lookup"><span data-stu-id="ee8c3-109">PARAMETERS</span></span>

### <span data-ttu-id="ee8c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8c3-110">-DefaultProfile</span></span>
<span data-ttu-id="ee8c3-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee8c3-112">-Chave</span><span class="sxs-lookup"><span data-stu-id="ee8c3-112">-Key</span></span>
<span data-ttu-id="ee8c3-113">Matriz de valores chave como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8c3-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ee8c3-114">-TtlInSeconds</span></span>
<span data-ttu-id="ee8c3-115">Número de segundos após o qual o índice expira.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="ee8c3-116">-Exclusivo</span><span class="sxs-lookup"><span data-stu-id="ee8c3-116">-Unique</span></span>
<span data-ttu-id="ee8c3-117">Bool para indicar se o índice é exclusivo ou não.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="ee8c3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8c3-118">CommonParameters</span></span>
<span data-ttu-id="ee8c3-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee8c3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8c3-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee8c3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8c3-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee8c3-121">INPUTS</span></span>

### <span data-ttu-id="ee8c3-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ee8c3-122">None</span></span>

## <span data-ttu-id="ee8c3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee8c3-123">OUTPUTS</span></span>

### <span data-ttu-id="ee8c3-124">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="ee8c3-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="ee8c3-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee8c3-125">NOTES</span></span>

## <span data-ttu-id="ee8c3-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee8c3-126">RELATED LINKS</span></span>
