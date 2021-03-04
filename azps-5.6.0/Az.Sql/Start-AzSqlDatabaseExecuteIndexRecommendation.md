---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 74beb667ec01af4661c2f56daa6a3159d960622a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888423"
---
# <span data-ttu-id="ce49b-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce49b-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ce49b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce49b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce49b-103">Inicia o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="ce49b-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ce49b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce49b-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce49b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce49b-105">DESCRIPTION</span></span>
<span data-ttu-id="ce49b-106">O cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** inicia o fluxo de trabalho que executa uma operação de índice recomendada para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ce49b-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="ce49b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce49b-107">EXAMPLES</span></span>

### <span data-ttu-id="ce49b-108">Exemplo 1: Executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="ce49b-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ce49b-109">Este comando executa uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="ce49b-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="ce49b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce49b-110">PARAMETERS</span></span>

### <span data-ttu-id="ce49b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce49b-111">-DatabaseName</span></span>
<span data-ttu-id="ce49b-112">Especifica o nome do banco de dados para o qual este cmdlet inicia o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce49b-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce49b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce49b-113">-DefaultProfile</span></span>
<span data-ttu-id="ce49b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ce49b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce49b-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ce49b-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ce49b-116">Especifica o nome da recomendação de índice que este cmdlet executa.</span><span class="sxs-lookup"><span data-stu-id="ce49b-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce49b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce49b-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce49b-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="ce49b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce49b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce49b-119">-ServerName</span></span>
<span data-ttu-id="ce49b-120">Especifica o servidor que hospeda o banco de dados para o qual este cmdlet inicia um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce49b-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce49b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce49b-121">CommonParameters</span></span>
<span data-ttu-id="ce49b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce49b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce49b-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce49b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce49b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce49b-124">INPUTS</span></span>

### <span data-ttu-id="ce49b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ce49b-125">System.String</span></span>

## <span data-ttu-id="ce49b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce49b-126">OUTPUTS</span></span>

### <span data-ttu-id="ce49b-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce49b-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ce49b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce49b-128">NOTES</span></span>

## <span data-ttu-id="ce49b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce49b-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce49b-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce49b-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="ce49b-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce49b-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ce49b-132">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="ce49b-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


