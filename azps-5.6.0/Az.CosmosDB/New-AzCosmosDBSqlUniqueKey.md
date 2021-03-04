---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890283"
---
# <span data-ttu-id="c0fc0-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="c0fc0-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="c0fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fc0-103">Cria um novo objeto Sql UniqueKey do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c0fc0-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="c0fc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0fc0-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0fc0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fc0-106">O cmdlet **New-AzCosmosDBSqlUniqueKey** cria um novo objeto do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="c0fc0-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="c0fc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="c0fc0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0fc0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="c0fc0-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-109">PARAMETERS</span></span>

### <span data-ttu-id="c0fc0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fc0-110">-DefaultProfile</span></span>
<span data-ttu-id="c0fc0-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0fc0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0fc0-112">-Path</span><span class="sxs-lookup"><span data-stu-id="c0fc0-112">-Path</span></span>
<span data-ttu-id="c0fc0-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="c0fc0-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fc0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fc0-114">CommonParameters</span></span>
<span data-ttu-id="c0fc0-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fc0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fc0-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0fc0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fc0-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-117">INPUTS</span></span>

### <span data-ttu-id="c0fc0-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c0fc0-118">None</span></span>

## <span data-ttu-id="c0fc0-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-119">OUTPUTS</span></span>

### <span data-ttu-id="c0fc0-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="c0fc0-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="c0fc0-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0fc0-121">NOTES</span></span>

## <span data-ttu-id="c0fc0-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0fc0-122">RELATED LINKS</span></span>
