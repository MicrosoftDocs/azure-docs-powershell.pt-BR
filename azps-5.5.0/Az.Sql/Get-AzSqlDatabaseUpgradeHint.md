---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111344"
---
# <span data-ttu-id="3b51e-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="3b51e-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="3b51e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b51e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b51e-103">Obtém dicas de nível de preços para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b51e-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="3b51e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b51e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b51e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b51e-105">DESCRIPTION</span></span>
<span data-ttu-id="3b51e-106">O cmdlet **Get-AzSqlDatabaseUpgradeHint obtém** dicas de nível de preço para atualizar um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b51e-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="3b51e-107">Bancos de dados que ainda estão em níveis de preços da Web e do Business têm a dica para atualizar para as novas camadas de preços Básico, Padrão ou Premium.</span><span class="sxs-lookup"><span data-stu-id="3b51e-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="3b51e-108">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="3b51e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3b51e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b51e-109">EXAMPLES</span></span>

### <span data-ttu-id="3b51e-110">Exemplo 1: Obter recomendações para todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="3b51e-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3b51e-111">Esse comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="3b51e-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="3b51e-112">Exemplo 2: Obter recomendações para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="3b51e-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="3b51e-113">Esse comando retorna dicas de atualização para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="3b51e-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="3b51e-114">Exemplo 3: Obter recomendação para todos os bancos de dados que não estão em um pool de banco de dados elástica</span><span class="sxs-lookup"><span data-stu-id="3b51e-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="3b51e-115">Esse comando retorna dicas de atualização para todos os bancos de dados que não estão em um pool de banco de dados elástica.</span><span class="sxs-lookup"><span data-stu-id="3b51e-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="3b51e-116">Exemplo 4: obter recomendações para todos os bancos de dados em um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="3b51e-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="3b51e-117">Esse comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01 que começam com "Banco de Dados".</span><span class="sxs-lookup"><span data-stu-id="3b51e-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="3b51e-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b51e-118">PARAMETERS</span></span>

### <span data-ttu-id="3b51e-119">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="3b51e-119">-DatabaseName</span></span>
<span data-ttu-id="3b51e-120">Especifica o nome do banco de dados SQL para o qual este cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="3b51e-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="3b51e-121">Se você não especificar um banco de dados, esse cmdlet obtém dicas para todos os bancos de dados no servidor lógico.</span><span class="sxs-lookup"><span data-stu-id="3b51e-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="3b51e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b51e-122">-DefaultProfile</span></span>
<span data-ttu-id="3b51e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3b51e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b51e-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="3b51e-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="3b51e-125">Indica se os bancos de dados em pools de banco de dados elásticas são excluídos das recomendações retornadas.</span><span class="sxs-lookup"><span data-stu-id="3b51e-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="3b51e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b51e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b51e-127">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="3b51e-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3b51e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b51e-128">-ServerName</span></span>
<span data-ttu-id="3b51e-129">Especifica o nome do servidor que hospeda o banco de dados para o qual este cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="3b51e-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="3b51e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3b51e-130">-Confirm</span></span>
<span data-ttu-id="3b51e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b51e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b51e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b51e-132">-WhatIf</span></span>
<span data-ttu-id="3b51e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3b51e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b51e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b51e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b51e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b51e-135">CommonParameters</span></span>
<span data-ttu-id="3b51e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b51e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b51e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b51e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b51e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b51e-138">INPUTS</span></span>

### <span data-ttu-id="3b51e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3b51e-139">System.String</span></span>

### <span data-ttu-id="3b51e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b51e-140">System.Boolean</span></span>

## <span data-ttu-id="3b51e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b51e-141">OUTPUTS</span></span>

### <span data-ttu-id="3b51e-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="3b51e-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="3b51e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="3b51e-143">NOTES</span></span>

## <span data-ttu-id="3b51e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b51e-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b51e-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="3b51e-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="3b51e-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="3b51e-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


