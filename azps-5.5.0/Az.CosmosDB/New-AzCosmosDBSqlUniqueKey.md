---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116869"
---
# <span data-ttu-id="0af2d-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0af2d-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="0af2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0af2d-102">SYNOPSIS</span></span>
<span data-ttu-id="0af2d-103">Cria um novo objeto Sql UniqueKey do Sql Sql.</span><span class="sxs-lookup"><span data-stu-id="0af2d-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="0af2d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0af2d-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af2d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0af2d-105">DESCRIPTION</span></span>
<span data-ttu-id="0af2d-106">O **cmdlet New-AzCosmosDBSqlUniqueKey** cria um novo objeto do tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="0af2d-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="0af2d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0af2d-107">EXAMPLES</span></span>

### <span data-ttu-id="0af2d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0af2d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="0af2d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0af2d-109">PARAMETERS</span></span>

### <span data-ttu-id="0af2d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af2d-110">-DefaultProfile</span></span>
<span data-ttu-id="0af2d-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0af2d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af2d-112">-Caminho</span><span class="sxs-lookup"><span data-stu-id="0af2d-112">-Path</span></span>
<span data-ttu-id="0af2d-113">Matriz de cadeia de caracteres de valores de caminho</span><span class="sxs-lookup"><span data-stu-id="0af2d-113">Array of string of path values</span></span>

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

### <span data-ttu-id="0af2d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af2d-114">CommonParameters</span></span>
<span data-ttu-id="0af2d-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af2d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af2d-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0af2d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af2d-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="0af2d-117">INPUTS</span></span>

### <span data-ttu-id="0af2d-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0af2d-118">None</span></span>

## <span data-ttu-id="0af2d-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="0af2d-119">OUTPUTS</span></span>

### <span data-ttu-id="0af2d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0af2d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="0af2d-121">Notas</span><span class="sxs-lookup"><span data-stu-id="0af2d-121">NOTES</span></span>

## <span data-ttu-id="0af2d-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0af2d-122">RELATED LINKS</span></span>
