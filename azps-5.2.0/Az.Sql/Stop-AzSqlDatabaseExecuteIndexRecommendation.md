---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260392"
---
# <span data-ttu-id="c2b75-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2b75-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="c2b75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2b75-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b75-103">Interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="c2b75-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="c2b75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2b75-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2b75-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b75-106">O cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="c2b75-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="c2b75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2b75-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b75-108">Exemplo 1: parar de executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="c2b75-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c2b75-109">Esse comando para de executar uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="c2b75-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="c2b75-110">OS</span><span class="sxs-lookup"><span data-stu-id="c2b75-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b75-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2b75-111">-DatabaseName</span></span>
<span data-ttu-id="c2b75-112">Especifica o nome do banco de dados para o qual esse cmdlet interrompe o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2b75-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="c2b75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b75-113">-DefaultProfile</span></span>
<span data-ttu-id="c2b75-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c2b75-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2b75-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c2b75-115">-IndexRecommendationName</span></span>
<span data-ttu-id="c2b75-116">Especifica o nome da recomendação de índice que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="c2b75-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c2b75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b75-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2b75-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c2b75-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c2b75-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c2b75-119">-ServerName</span></span>
<span data-ttu-id="c2b75-120">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet interrompe um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2b75-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="c2b75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b75-121">CommonParameters</span></span>
<span data-ttu-id="c2b75-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b75-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b75-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b75-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2b75-124">INPUTS</span></span>

### <span data-ttu-id="c2b75-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b75-125">System.String</span></span>

## <span data-ttu-id="c2b75-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2b75-126">OUTPUTS</span></span>

### <span data-ttu-id="c2b75-127">Microsoft. Azure. Commands. Sql. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2b75-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="c2b75-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2b75-128">NOTES</span></span>

## <span data-ttu-id="c2b75-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2b75-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2b75-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2b75-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="c2b75-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2b75-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c2b75-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c2b75-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


