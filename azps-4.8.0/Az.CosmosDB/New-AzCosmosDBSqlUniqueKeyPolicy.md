---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112865"
---
# <span data-ttu-id="1b7ec-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1b7ec-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="1b7ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7ec-103">Cria um novo objeto CosmosDB SqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b7ec-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="1b7ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b7ec-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b7ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1b7ec-106">O cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** cria um novo objeto do tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="1b7ec-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="1b7ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b7ec-107">EXAMPLES</span></span>

### <span data-ttu-id="1b7ec-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b7ec-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="1b7ec-109">OS</span><span class="sxs-lookup"><span data-stu-id="1b7ec-109">PARAMETERS</span></span>

### <span data-ttu-id="1b7ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7ec-110">-DefaultProfile</span></span>
<span data-ttu-id="1b7ec-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b7ec-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b7ec-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="1b7ec-112">-UniqueKey</span></span>
<span data-ttu-id="1b7ec-113">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1b7ec-113">Database name.</span></span>

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

### <span data-ttu-id="1b7ec-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7ec-114">CommonParameters</span></span>
<span data-ttu-id="1b7ec-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b7ec-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7ec-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b7ec-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7ec-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b7ec-117">INPUTS</span></span>

### <span data-ttu-id="1b7ec-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1b7ec-118">None</span></span>

## <span data-ttu-id="1b7ec-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b7ec-119">OUTPUTS</span></span>

### <span data-ttu-id="1b7ec-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1b7ec-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="1b7ec-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b7ec-121">NOTES</span></span>

## <span data-ttu-id="1b7ec-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b7ec-122">RELATED LINKS</span></span>
