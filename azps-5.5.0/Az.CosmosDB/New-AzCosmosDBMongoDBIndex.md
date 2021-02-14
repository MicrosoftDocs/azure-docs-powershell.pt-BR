---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115911"
---
# <span data-ttu-id="3ed31-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="3ed31-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="3ed31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ed31-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed31-103">Cria um novo Índice MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3ed31-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="3ed31-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed31-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed31-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ed31-105">DESCRIPTION</span></span>
<span data-ttu-id="3ed31-106">O **New-AzCosmosDBMongoDBIndex cria** um novo Índice MongoDB.</span><span class="sxs-lookup"><span data-stu-id="3ed31-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="3ed31-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ed31-107">EXAMPLES</span></span>

### <span data-ttu-id="3ed31-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ed31-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="3ed31-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed31-109">PARAMETERS</span></span>

### <span data-ttu-id="3ed31-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed31-110">-DefaultProfile</span></span>
<span data-ttu-id="3ed31-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed31-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed31-112">-Tecla</span><span class="sxs-lookup"><span data-stu-id="3ed31-112">-Key</span></span>
<span data-ttu-id="3ed31-113">Matriz de valores principais como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3ed31-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="3ed31-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="3ed31-114">-TtlInSeconds</span></span>
<span data-ttu-id="3ed31-115">Número de segundos após os quais o índice expira.</span><span class="sxs-lookup"><span data-stu-id="3ed31-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="3ed31-116">-Exclusivo</span><span class="sxs-lookup"><span data-stu-id="3ed31-116">-Unique</span></span>
<span data-ttu-id="3ed31-117">Bool para indicar se o índice é exclusivo ou não.</span><span class="sxs-lookup"><span data-stu-id="3ed31-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="3ed31-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed31-118">CommonParameters</span></span>
<span data-ttu-id="3ed31-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed31-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed31-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ed31-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed31-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ed31-121">INPUTS</span></span>

### <span data-ttu-id="3ed31-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ed31-122">None</span></span>

## <span data-ttu-id="3ed31-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ed31-123">OUTPUTS</span></span>

### <span data-ttu-id="3ed31-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="3ed31-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="3ed31-125">Notas</span><span class="sxs-lookup"><span data-stu-id="3ed31-125">NOTES</span></span>

## <span data-ttu-id="3ed31-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ed31-126">RELATED LINKS</span></span>
