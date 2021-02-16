---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118599"
---
# <span data-ttu-id="58ac5-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="58ac5-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="58ac5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="58ac5-103">Interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="58ac5-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="58ac5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58ac5-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58ac5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="58ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="58ac5-106">O cmdlet **Stop-AzSqlDatabaseExecuteIndexRecommendation** interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="58ac5-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="58ac5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58ac5-107">EXAMPLES</span></span>

### <span data-ttu-id="58ac5-108">Exemplo 1: parar de executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="58ac5-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="58ac5-109">Esse comando para de executar uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="58ac5-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="58ac5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58ac5-110">PARAMETERS</span></span>

### <span data-ttu-id="58ac5-111">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="58ac5-111">-DatabaseName</span></span>
<span data-ttu-id="58ac5-112">Especifica o nome do banco de dados para o qual esse cmdlet interrompe o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="58ac5-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="58ac5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ac5-113">-DefaultProfile</span></span>
<span data-ttu-id="58ac5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="58ac5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58ac5-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="58ac5-115">-IndexRecommendationName</span></span>
<span data-ttu-id="58ac5-116">Especifica o nome da recomendação de índice que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="58ac5-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="58ac5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ac5-117">-ResourceGroupName</span></span>
<span data-ttu-id="58ac5-118">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="58ac5-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="58ac5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58ac5-119">-ServerName</span></span>
<span data-ttu-id="58ac5-120">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet interrompe um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="58ac5-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="58ac5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ac5-121">CommonParameters</span></span>
<span data-ttu-id="58ac5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ac5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ac5-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58ac5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ac5-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="58ac5-124">INPUTS</span></span>

### <span data-ttu-id="58ac5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="58ac5-125">System.String</span></span>

## <span data-ttu-id="58ac5-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="58ac5-126">OUTPUTS</span></span>

### <span data-ttu-id="58ac5-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="58ac5-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="58ac5-128">Notas</span><span class="sxs-lookup"><span data-stu-id="58ac5-128">NOTES</span></span>

## <span data-ttu-id="58ac5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58ac5-129">RELATED LINKS</span></span>

[<span data-ttu-id="58ac5-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="58ac5-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="58ac5-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="58ac5-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="58ac5-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="58ac5-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


