---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260862"
---
# <span data-ttu-id="c5344-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c5344-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="c5344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5344-102">SYNOPSIS</span></span>
<span data-ttu-id="c5344-103">Cria um novo objeto CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c5344-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="c5344-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5344-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5344-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5344-105">DESCRIPTION</span></span>
<span data-ttu-id="c5344-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c5344-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="c5344-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5344-107">EXAMPLES</span></span>

### <span data-ttu-id="c5344-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5344-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="c5344-109">OS</span><span class="sxs-lookup"><span data-stu-id="c5344-109">PARAMETERS</span></span>

### <span data-ttu-id="c5344-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5344-110">-DefaultProfile</span></span>
<span data-ttu-id="c5344-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5344-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5344-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="c5344-112">-UniqueKey</span></span>
<span data-ttu-id="c5344-113">Matriz de objetos do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="c5344-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5344-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5344-114">CommonParameters</span></span>
<span data-ttu-id="c5344-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5344-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5344-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5344-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5344-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5344-117">INPUTS</span></span>

### <span data-ttu-id="c5344-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c5344-118">None</span></span>

## <span data-ttu-id="c5344-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5344-119">OUTPUTS</span></span>

### <span data-ttu-id="c5344-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c5344-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="c5344-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5344-121">NOTES</span></span>

## <span data-ttu-id="c5344-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5344-122">RELATED LINKS</span></span>
