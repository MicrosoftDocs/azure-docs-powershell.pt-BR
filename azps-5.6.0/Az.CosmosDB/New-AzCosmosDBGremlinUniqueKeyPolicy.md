---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886066"
---
# <span data-ttu-id="71094-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="71094-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="71094-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71094-102">SYNOPSIS</span></span>
<span data-ttu-id="71094-103">Cria um novo objeto UniqueKeyPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="71094-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="71094-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71094-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71094-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71094-105">DESCRIPTION</span></span>
<span data-ttu-id="71094-106">O cmdlet **New-AzCosmosDBGremlinUniqueKeyPolicy** cria um novo objeto do tipo PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="71094-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="71094-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71094-107">EXAMPLES</span></span>

### <span data-ttu-id="71094-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71094-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="71094-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71094-109">PARAMETERS</span></span>

### <span data-ttu-id="71094-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71094-110">-DefaultProfile</span></span>
<span data-ttu-id="71094-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71094-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71094-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="71094-112">-UniqueKey</span></span>
<span data-ttu-id="71094-113">Matriz de objetos do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="71094-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="71094-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71094-114">CommonParameters</span></span>
<span data-ttu-id="71094-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71094-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71094-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71094-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71094-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71094-117">INPUTS</span></span>

### <span data-ttu-id="71094-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71094-118">None</span></span>

## <span data-ttu-id="71094-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71094-119">OUTPUTS</span></span>

### <span data-ttu-id="71094-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="71094-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="71094-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="71094-121">NOTES</span></span>

## <span data-ttu-id="71094-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71094-122">RELATED LINKS</span></span>
