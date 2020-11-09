---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281318"
---
# <span data-ttu-id="f061c-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f061c-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="f061c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f061c-102">SYNOPSIS</span></span>
<span data-ttu-id="f061c-103">Cria um novo objeto CosmosDB UniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f061c-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="f061c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f061c-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f061c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f061c-105">DESCRIPTION</span></span>
<span data-ttu-id="f061c-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f061c-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="f061c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f061c-107">EXAMPLES</span></span>

### <span data-ttu-id="f061c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f061c-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="f061c-109">OS</span><span class="sxs-lookup"><span data-stu-id="f061c-109">PARAMETERS</span></span>

### <span data-ttu-id="f061c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f061c-110">-DefaultProfile</span></span>
<span data-ttu-id="f061c-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f061c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f061c-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="f061c-112">-UniqueKey</span></span>
<span data-ttu-id="f061c-113">Matriz de objetos do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="f061c-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="f061c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f061c-114">CommonParameters</span></span>
<span data-ttu-id="f061c-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f061c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f061c-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f061c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f061c-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f061c-117">INPUTS</span></span>

### <span data-ttu-id="f061c-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f061c-118">None</span></span>

## <span data-ttu-id="f061c-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f061c-119">OUTPUTS</span></span>

### <span data-ttu-id="f061c-120">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f061c-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="f061c-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f061c-121">NOTES</span></span>

## <span data-ttu-id="f061c-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f061c-122">RELATED LINKS</span></span>
