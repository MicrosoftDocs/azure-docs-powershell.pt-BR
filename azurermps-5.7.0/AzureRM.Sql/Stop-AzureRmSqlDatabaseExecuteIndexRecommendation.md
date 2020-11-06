---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603207"
---
# <span data-ttu-id="83864-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="83864-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="83864-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83864-102">SYNOPSIS</span></span>
<span data-ttu-id="83864-103">Interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="83864-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83864-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83864-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83864-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83864-105">DESCRIPTION</span></span>
<span data-ttu-id="83864-106">O cmdlet **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** interrompe o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="83864-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="83864-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83864-107">EXAMPLES</span></span>

### <span data-ttu-id="83864-108">Exemplo 1: parar de executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="83864-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="83864-109">Esse comando para de executar uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="83864-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="83864-110">OS</span><span class="sxs-lookup"><span data-stu-id="83864-110">PARAMETERS</span></span>

### <span data-ttu-id="83864-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83864-111">-DatabaseName</span></span>
<span data-ttu-id="83864-112">Especifica o nome do banco de dados para o qual esse cmdlet interrompe o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="83864-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83864-113">-DefaultProfile</span></span>
<span data-ttu-id="83864-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="83864-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83864-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="83864-115">-IndexRecommendationName</span></span>
<span data-ttu-id="83864-116">Especifica o nome da recomendação de índice que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="83864-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83864-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83864-117">-ResourceGroupName</span></span>
<span data-ttu-id="83864-118">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="83864-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83864-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="83864-119">-ServerName</span></span>
<span data-ttu-id="83864-120">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet interrompe um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="83864-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83864-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83864-121">CommonParameters</span></span>
<span data-ttu-id="83864-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83864-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83864-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83864-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83864-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83864-124">INPUTS</span></span>

### <span data-ttu-id="83864-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="83864-125">None</span></span>
<span data-ttu-id="83864-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="83864-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83864-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83864-127">OUTPUTS</span></span>

## <span data-ttu-id="83864-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83864-128">NOTES</span></span>

## <span data-ttu-id="83864-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83864-129">RELATED LINKS</span></span>

[<span data-ttu-id="83864-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="83864-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="83864-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="83864-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="83864-132">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="83864-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


