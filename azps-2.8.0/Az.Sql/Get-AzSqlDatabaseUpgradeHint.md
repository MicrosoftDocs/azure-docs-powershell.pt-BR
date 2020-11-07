---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773649"
---
# <span data-ttu-id="e7ddb-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="e7ddb-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="e7ddb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ddb-103">Obtém dicas de camada de preço para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="e7ddb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7ddb-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ddb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ddb-106">O cmdlet **Get-AzSqlDatabaseUpgradeHint** Obtém dicas de camada de preços para a atualização de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="e7ddb-107">Os bancos de dados que ainda estão em níveis de preços da Web e de negócios recebem a dica de atualização para os novos níveis de preços básico, padrão ou Premium.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="e7ddb-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e7ddb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7ddb-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ddb-110">Exemplo 1: obter recomendações para todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="e7ddb-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e7ddb-111">Esse comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="e7ddb-112">Exemplo 2: obter recomendações para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="e7ddb-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e7ddb-113">Esse comando retorna dicas de atualização para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="e7ddb-114">Exemplo 3: obter recomendação para todos os bancos de dados que não estão em um pool de banco de dados elástico</span><span class="sxs-lookup"><span data-stu-id="e7ddb-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="e7ddb-115">Esse comando retorna dicas de atualização para todos os bancos de dados que não estão em um pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="e7ddb-116">Exemplo 4: obter recomendações para todos os bancos de dados em um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="e7ddb-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="e7ddb-117">Esse comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01 que começam com "banco de dados".</span><span class="sxs-lookup"><span data-stu-id="e7ddb-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="e7ddb-118">OS</span><span class="sxs-lookup"><span data-stu-id="e7ddb-118">PARAMETERS</span></span>

### <span data-ttu-id="e7ddb-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7ddb-119">-DatabaseName</span></span>
<span data-ttu-id="e7ddb-120">Especifica o nome do banco de dados SQL para o qual esse cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="e7ddb-121">Se você não especificar um banco de dados, esse cmdlet receberá dicas para todos os bancos de dados no servidor lógico.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e7ddb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ddb-122">-DefaultProfile</span></span>
<span data-ttu-id="e7ddb-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e7ddb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7ddb-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="e7ddb-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="e7ddb-125">Indica se os bancos de dados em pools de bancos de dados elásticos estão excluídos das recomendações retornadas.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="e7ddb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ddb-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7ddb-127">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e7ddb-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e7ddb-128">-ServerName</span></span>
<span data-ttu-id="e7ddb-129">Especifica o nome do servidor que hospeda o banco de dados para o qual esse cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="e7ddb-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7ddb-130">-Confirm</span></span>
<span data-ttu-id="e7ddb-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ddb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ddb-132">-WhatIf</span></span>
<span data-ttu-id="e7ddb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ddb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ddb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ddb-135">CommonParameters</span></span>
<span data-ttu-id="e7ddb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ddb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ddb-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ddb-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ddb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7ddb-138">INPUTS</span></span>

### <span data-ttu-id="e7ddb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ddb-139">System.String</span></span>

### <span data-ttu-id="e7ddb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7ddb-140">System.Boolean</span></span>

## <span data-ttu-id="e7ddb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7ddb-141">OUTPUTS</span></span>

### <span data-ttu-id="e7ddb-142">Microsoft. Azure. Management. Sql. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="e7ddb-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="e7ddb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7ddb-143">NOTES</span></span>

## <span data-ttu-id="e7ddb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7ddb-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7ddb-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="e7ddb-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="e7ddb-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="e7ddb-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

