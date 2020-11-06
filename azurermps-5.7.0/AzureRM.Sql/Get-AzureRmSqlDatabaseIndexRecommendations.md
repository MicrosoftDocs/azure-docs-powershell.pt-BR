---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseindexrecommendations
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: 6e9622565017f71c8b73e70e7aa4d0c3528bc254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426567"
---
# <span data-ttu-id="81174-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="81174-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="81174-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81174-102">SYNOPSIS</span></span>
<span data-ttu-id="81174-103">Obtém as operações de índice recomendadas para um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81174-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81174-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81174-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81174-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81174-105">DESCRIPTION</span></span>
<span data-ttu-id="81174-106">O cmdlet **Get-AzureRmSqlDatabaseIndexRecommendations** Obtém as operações de índice recomendadas para um banco de dados ou um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="81174-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="81174-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81174-107">EXAMPLES</span></span>

### <span data-ttu-id="81174-108">Exemplo 1: obter recomendações de índice para todos os bancos de dados no servidor</span><span class="sxs-lookup"><span data-stu-id="81174-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="81174-109">Esse comando retorna recomendações de índice para todos os bancos de dados no Server Server01.</span><span class="sxs-lookup"><span data-stu-id="81174-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="81174-110">Exemplo 2: obter recomendações de índice para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="81174-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="81174-111">Esse comando retorna recomendações de índice para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="81174-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="81174-112">Exemplo 3: obter uma única recomendação de índice por nome</span><span class="sxs-lookup"><span data-stu-id="81174-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="81174-113">Esse comando retorna a recomendação de índice único por nome.</span><span class="sxs-lookup"><span data-stu-id="81174-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="81174-114">OS</span><span class="sxs-lookup"><span data-stu-id="81174-114">PARAMETERS</span></span>

### <span data-ttu-id="81174-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81174-115">-DatabaseName</span></span>
<span data-ttu-id="81174-116">Especifica o nome do banco de dados para o qual este cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="81174-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81174-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81174-117">-DefaultProfile</span></span>
<span data-ttu-id="81174-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="81174-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81174-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="81174-119">-IndexRecommendationName</span></span>
<span data-ttu-id="81174-120">Especifica o nome da recomendação de índice que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="81174-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81174-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81174-121">-ResourceGroupName</span></span>
<span data-ttu-id="81174-122">Especifica o nome do grupo de recursos para o qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="81174-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="81174-123">Este cmdlet obtém recomendações de índice para um banco de dados hospedado por esse servidor.</span><span class="sxs-lookup"><span data-stu-id="81174-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="81174-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="81174-124">-ServerName</span></span>
<span data-ttu-id="81174-125">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="81174-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="81174-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="81174-126">-TableName</span></span>
<span data-ttu-id="81174-127">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="81174-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81174-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81174-128">-Confirm</span></span>
<span data-ttu-id="81174-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81174-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81174-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81174-130">-WhatIf</span></span>
<span data-ttu-id="81174-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81174-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81174-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81174-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81174-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81174-133">CommonParameters</span></span>
<span data-ttu-id="81174-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81174-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81174-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81174-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81174-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81174-136">INPUTS</span></span>

### <span data-ttu-id="81174-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="81174-137">None</span></span>
<span data-ttu-id="81174-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="81174-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81174-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81174-139">OUTPUTS</span></span>

## <span data-ttu-id="81174-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81174-140">NOTES</span></span>

## <span data-ttu-id="81174-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81174-141">RELATED LINKS</span></span>

[<span data-ttu-id="81174-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="81174-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="81174-143">Parar-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="81174-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
