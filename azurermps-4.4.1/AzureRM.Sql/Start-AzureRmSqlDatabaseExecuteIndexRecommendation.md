---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610152"
---
# <span data-ttu-id="81a1a-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="81a1a-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="81a1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="81a1a-103">Inicia o fluxo de trabalho que executa uma operação de índice recomendada.</span><span class="sxs-lookup"><span data-stu-id="81a1a-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81a1a-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81a1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="81a1a-106">O cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** inicia o fluxo de trabalho que executa uma operação de indexação recomendada para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="81a1a-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="81a1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="81a1a-108">Exemplo 1: executar uma recomendação de índice</span><span class="sxs-lookup"><span data-stu-id="81a1a-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="81a1a-109">Esse comando executa uma recomendação de índice.</span><span class="sxs-lookup"><span data-stu-id="81a1a-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="81a1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="81a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="81a1a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81a1a-111">-DatabaseName</span></span>
<span data-ttu-id="81a1a-112">Especifica o nome do banco de dados para o qual esse cmdlet inicia o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81a1a-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="81a1a-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="81a1a-113">-IndexRecommendationName</span></span>
<span data-ttu-id="81a1a-114">Especifica o nome da recomendação de índice que este cmdlet executa.</span><span class="sxs-lookup"><span data-stu-id="81a1a-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="81a1a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a1a-115">-ResourceGroupName</span></span>
<span data-ttu-id="81a1a-116">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="81a1a-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="81a1a-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="81a1a-117">-ServerName</span></span>
<span data-ttu-id="81a1a-118">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet inicia um fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81a1a-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="81a1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a1a-119">-DefaultProfile</span></span>
<span data-ttu-id="81a1a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81a1a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a1a-121">CommonParameters</span></span>
<span data-ttu-id="81a1a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a1a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a1a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a1a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81a1a-124">INPUTS</span></span>

## <span data-ttu-id="81a1a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81a1a-125">OUTPUTS</span></span>

## <span data-ttu-id="81a1a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81a1a-126">NOTES</span></span>

## <span data-ttu-id="81a1a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81a1a-127">RELATED LINKS</span></span>

[<span data-ttu-id="81a1a-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="81a1a-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="81a1a-129">Parar-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="81a1a-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="81a1a-130">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="81a1a-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


