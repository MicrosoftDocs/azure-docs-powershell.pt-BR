---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b289dc637b3d75321120f06eb9ddf604ebcdabba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603429"
---
# <span data-ttu-id="f4527-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="f4527-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="f4527-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4527-102">SYNOPSIS</span></span>
<span data-ttu-id="f4527-103">Obtém dicas de camada de preço para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f4527-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4527-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4527-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4527-105">DESCRIPTION</span></span>
<span data-ttu-id="f4527-106">O cmdlet **Get-AzureRmSqlDatabaseUpgradeHint** Obtém dicas de camada de preços para a atualização de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4527-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="f4527-107">Os bancos de dados que ainda estão em níveis de preços da Web e de negócios recebem a dica de atualização para os novos níveis de preços básico, padrão ou Premium.</span><span class="sxs-lookup"><span data-stu-id="f4527-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="f4527-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="f4527-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f4527-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4527-109">EXAMPLES</span></span>

### <span data-ttu-id="f4527-110">Exemplo 1: obter recomendações para todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="f4527-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f4527-111">Esse comando retorna dicas de atualização para todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="f4527-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="f4527-112">Exemplo 2: obter recomendações para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="f4527-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f4527-113">Esse comando retorna dicas de atualização para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="f4527-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="f4527-114">Exemplo 3: obter recomendação para todos os bancos de dados que não estão em um pool de banco de dados elástico</span><span class="sxs-lookup"><span data-stu-id="f4527-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="f4527-115">Esse comando retorna dicas de atualização para todos os bancos de dados que não estão em um pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="f4527-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="f4527-116">OS</span><span class="sxs-lookup"><span data-stu-id="f4527-116">PARAMETERS</span></span>

### <span data-ttu-id="f4527-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4527-117">-DatabaseName</span></span>
<span data-ttu-id="f4527-118">Especifica o nome do banco de dados SQL para o qual esse cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="f4527-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="f4527-119">Se você não especificar um banco de dados, esse cmdlet receberá dicas para todos os bancos de dados no servidor lógico.</span><span class="sxs-lookup"><span data-stu-id="f4527-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="f4527-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4527-120">-DefaultProfile</span></span>
<span data-ttu-id="f4527-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f4527-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4527-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="f4527-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="f4527-123">Indica se os bancos de dados em pools de bancos de dados elásticos estão excluídos das recomendações retornadas.</span><span class="sxs-lookup"><span data-stu-id="f4527-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="f4527-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4527-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4527-125">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f4527-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f4527-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f4527-126">-ServerName</span></span>
<span data-ttu-id="f4527-127">Especifica o nome do servidor que hospeda o banco de dados para o qual esse cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="f4527-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="f4527-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4527-128">-Confirm</span></span>
<span data-ttu-id="f4527-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4527-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4527-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4527-130">-WhatIf</span></span>
<span data-ttu-id="f4527-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4527-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4527-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4527-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4527-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4527-133">CommonParameters</span></span>
<span data-ttu-id="f4527-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4527-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4527-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4527-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4527-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4527-136">INPUTS</span></span>

### <span data-ttu-id="f4527-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f4527-137">System.String</span></span>

### <span data-ttu-id="f4527-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4527-138">System.Boolean</span></span>

## <span data-ttu-id="f4527-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4527-139">OUTPUTS</span></span>

### <span data-ttu-id="f4527-140">Microsoft. Azure. Management. Sql. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="f4527-140">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="f4527-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4527-141">NOTES</span></span>

## <span data-ttu-id="f4527-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4527-142">RELATED LINKS</span></span>

[<span data-ttu-id="f4527-143">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f4527-143">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="f4527-144">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="f4527-144">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


