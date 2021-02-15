---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114461"
---
# <span data-ttu-id="3cdfe-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3cdfe-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="3cdfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cdfe-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdfe-103">Inicia o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="3cdfe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cdfe-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cdfe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cdfe-105">DESCRIPTION</span></span>
<span data-ttu-id="3cdfe-106">O cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** inicia o fluxo de trabalho que executa uma operação de índice recomendada para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="3cdfe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3cdfe-107">EXAMPLES</span></span>

### <span data-ttu-id="3cdfe-108">Exemplo 1: Executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="3cdfe-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="3cdfe-109">Esse comando executa uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="3cdfe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cdfe-110">PARAMETERS</span></span>

### <span data-ttu-id="3cdfe-111">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="3cdfe-111">-DatabaseName</span></span>
<span data-ttu-id="3cdfe-112">Especifica o nome do banco de dados para o qual esse cmdlet inicia o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="3cdfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdfe-113">-DefaultProfile</span></span>
<span data-ttu-id="3cdfe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3cdfe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cdfe-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="3cdfe-115">-IndexRecommendationName</span></span>
<span data-ttu-id="3cdfe-116">Especifica o nome da recomendação de índice que este cmdlet executa.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="3cdfe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cdfe-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cdfe-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3cdfe-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3cdfe-119">-ServerName</span></span>
<span data-ttu-id="3cdfe-120">Especifica o servidor que hospeda o banco de dados para o qual este cmdlet inicia um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="3cdfe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdfe-121">CommonParameters</span></span>
<span data-ttu-id="3cdfe-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdfe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdfe-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cdfe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdfe-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="3cdfe-124">INPUTS</span></span>

### <span data-ttu-id="3cdfe-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3cdfe-125">System.String</span></span>

## <span data-ttu-id="3cdfe-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="3cdfe-126">OUTPUTS</span></span>

### <span data-ttu-id="3cdfe-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3cdfe-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="3cdfe-128">Notas</span><span class="sxs-lookup"><span data-stu-id="3cdfe-128">NOTES</span></span>

## <span data-ttu-id="3cdfe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cdfe-129">RELATED LINKS</span></span>

[<span data-ttu-id="3cdfe-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3cdfe-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="3cdfe-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="3cdfe-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="3cdfe-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3cdfe-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


