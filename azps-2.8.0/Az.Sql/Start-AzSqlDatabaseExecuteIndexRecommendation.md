---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c432b3a23c4495abebda013b5dd3943132827a30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774002"
---
# <span data-ttu-id="cd5ae-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="cd5ae-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="cd5ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5ae-103">Inicia o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="cd5ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd5ae-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd5ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="cd5ae-106">O cmdlet **Start-AzSqlDatabaseExecuteIndexRecommendation** inicia o fluxo de trabalho que executa uma operação de indexação recomendada para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="cd5ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="cd5ae-108">Exemplo 1: executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="cd5ae-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="cd5ae-109">Esse comando executa uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="cd5ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="cd5ae-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd5ae-111">-DatabaseName</span></span>
<span data-ttu-id="cd5ae-112">Especifica o nome do banco de dados para o qual esse cmdlet inicia o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="cd5ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5ae-113">-DefaultProfile</span></span>
<span data-ttu-id="cd5ae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cd5ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd5ae-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="cd5ae-115">-IndexRecommendationName</span></span>
<span data-ttu-id="cd5ae-116">Especifica o nome da recomendação de índice que este cmdlet executa.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="cd5ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd5ae-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cd5ae-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cd5ae-119">-ServerName</span></span>
<span data-ttu-id="cd5ae-120">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet inicia um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="cd5ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5ae-121">CommonParameters</span></span>
<span data-ttu-id="cd5ae-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5ae-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd5ae-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5ae-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd5ae-124">INPUTS</span></span>

### <span data-ttu-id="cd5ae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cd5ae-125">System.String</span></span>

## <span data-ttu-id="cd5ae-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd5ae-126">OUTPUTS</span></span>

### <span data-ttu-id="cd5ae-127">Microsoft. Azure. Commands. Sql. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="cd5ae-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="cd5ae-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd5ae-128">NOTES</span></span>

## <span data-ttu-id="cd5ae-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd5ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="cd5ae-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="cd5ae-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="cd5ae-131">Parar-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="cd5ae-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="cd5ae-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cd5ae-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


