---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889788"
---
# <span data-ttu-id="787ae-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="787ae-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="787ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787ae-102">SYNOPSIS</span></span>
<span data-ttu-id="787ae-103">Cria um novo objeto SqlUniqueKeyPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="787ae-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="787ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="787ae-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="787ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="787ae-105">DESCRIPTION</span></span>
<span data-ttu-id="787ae-106">O cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** cria um novo objeto do tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="787ae-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="787ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="787ae-107">EXAMPLES</span></span>

### <span data-ttu-id="787ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="787ae-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="787ae-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="787ae-109">PARAMETERS</span></span>

### <span data-ttu-id="787ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787ae-110">-DefaultProfile</span></span>
<span data-ttu-id="787ae-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="787ae-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787ae-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="787ae-112">-UniqueKey</span></span>
<span data-ttu-id="787ae-113">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="787ae-113">Database name.</span></span>

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

### <span data-ttu-id="787ae-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787ae-114">CommonParameters</span></span>
<span data-ttu-id="787ae-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787ae-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787ae-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787ae-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787ae-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="787ae-117">INPUTS</span></span>

### <span data-ttu-id="787ae-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="787ae-118">None</span></span>

## <span data-ttu-id="787ae-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="787ae-119">OUTPUTS</span></span>

### <span data-ttu-id="787ae-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="787ae-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="787ae-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="787ae-121">NOTES</span></span>

## <span data-ttu-id="787ae-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="787ae-122">RELATED LINKS</span></span>
