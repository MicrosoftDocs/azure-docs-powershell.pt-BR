---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901410"
---
# <span data-ttu-id="58884-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="58884-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="58884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58884-102">SYNOPSIS</span></span>
<span data-ttu-id="58884-103">Obtém dicas de camada de preços para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="58884-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="58884-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="58884-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58884-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="58884-105">DESCRIPTION</span></span>
<span data-ttu-id="58884-106">O cmdlet **Get-AzSqlDatabaseUpgradeHint** obtém dicas de camada de preços para atualizar um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="58884-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="58884-107">Os bancos de dados que ainda estão em camadas de preços da Web e do Business têm a dica para atualizar para as novas camadas de preços Básica, Padrão ou Premium.</span><span class="sxs-lookup"><span data-stu-id="58884-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="58884-108">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="58884-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="58884-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58884-109">EXAMPLES</span></span>

### <span data-ttu-id="58884-110">Exemplo 1: obter recomendações para todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="58884-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="58884-111">Este comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="58884-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="58884-112">Exemplo 2: obter recomendações para banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="58884-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="58884-113">Este comando retorna dicas de atualização para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="58884-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="58884-114">Exemplo 3: obter recomendação para todos os bancos de dados que não estão em um pool de banco de dados elástica</span><span class="sxs-lookup"><span data-stu-id="58884-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="58884-115">Este comando retorna dicas de atualização para todos os bancos de dados que não estão em um pool de banco de dados elástica.</span><span class="sxs-lookup"><span data-stu-id="58884-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="58884-116">Exemplo 4: obter recomendações para todos os bancos de dados em um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="58884-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="58884-117">Este comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01 que começam com "Database".</span><span class="sxs-lookup"><span data-stu-id="58884-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="58884-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="58884-118">PARAMETERS</span></span>

### <span data-ttu-id="58884-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58884-119">-DatabaseName</span></span>
<span data-ttu-id="58884-120">Especifica o nome do banco de dados SQL para o qual este cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="58884-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="58884-121">Se você não especificar um banco de dados, esse cmdlet obtém dicas para todos os bancos de dados no servidor lógico.</span><span class="sxs-lookup"><span data-stu-id="58884-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58884-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58884-122">-DefaultProfile</span></span>
<span data-ttu-id="58884-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="58884-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58884-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="58884-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="58884-125">Indica se bancos de dados em pools de bancos de dados elásticas são excluídos das recomendações retornadas.</span><span class="sxs-lookup"><span data-stu-id="58884-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58884-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58884-126">-ResourceGroupName</span></span>
<span data-ttu-id="58884-127">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="58884-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="58884-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58884-128">-ServerName</span></span>
<span data-ttu-id="58884-129">Especifica o nome do servidor que hospeda o banco de dados para o qual este cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="58884-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58884-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58884-130">-Confirm</span></span>
<span data-ttu-id="58884-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58884-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58884-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58884-132">-WhatIf</span></span>
<span data-ttu-id="58884-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58884-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58884-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58884-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58884-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58884-135">CommonParameters</span></span>
<span data-ttu-id="58884-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58884-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58884-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58884-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58884-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58884-138">INPUTS</span></span>

### <span data-ttu-id="58884-139">System.String</span><span class="sxs-lookup"><span data-stu-id="58884-139">System.String</span></span>

### <span data-ttu-id="58884-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58884-140">System.Boolean</span></span>

## <span data-ttu-id="58884-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="58884-141">OUTPUTS</span></span>

### <span data-ttu-id="58884-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="58884-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="58884-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="58884-143">NOTES</span></span>

## <span data-ttu-id="58884-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58884-144">RELATED LINKS</span></span>

[<span data-ttu-id="58884-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="58884-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="58884-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="58884-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


