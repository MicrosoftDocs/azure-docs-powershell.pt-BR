---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115908"
---
# <span data-ttu-id="64ad8-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="64ad8-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="64ad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="64ad8-103">Cria um novo objeto SqlUniqueKeyPolicy Do SqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="64ad8-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="64ad8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64ad8-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64ad8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="64ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="64ad8-106">O cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** cria um novo objeto do tipo PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="64ad8-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="64ad8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64ad8-107">EXAMPLES</span></span>

### <span data-ttu-id="64ad8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64ad8-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="64ad8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64ad8-109">PARAMETERS</span></span>

### <span data-ttu-id="64ad8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ad8-110">-DefaultProfile</span></span>
<span data-ttu-id="64ad8-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64ad8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ad8-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="64ad8-112">-UniqueKey</span></span>
<span data-ttu-id="64ad8-113">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="64ad8-113">Database name.</span></span>

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

### <span data-ttu-id="64ad8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ad8-114">CommonParameters</span></span>
<span data-ttu-id="64ad8-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ad8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ad8-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64ad8-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ad8-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="64ad8-117">INPUTS</span></span>

### <span data-ttu-id="64ad8-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="64ad8-118">None</span></span>

## <span data-ttu-id="64ad8-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="64ad8-119">OUTPUTS</span></span>

### <span data-ttu-id="64ad8-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="64ad8-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="64ad8-121">Notas</span><span class="sxs-lookup"><span data-stu-id="64ad8-121">NOTES</span></span>

## <span data-ttu-id="64ad8-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64ad8-122">RELATED LINKS</span></span>
