---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: fc75aa4f838d19044514d3e6c343e04cdbf1d9be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885798"
---
# <span data-ttu-id="b979e-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="b979e-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="b979e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b979e-102">SYNOPSIS</span></span>
<span data-ttu-id="b979e-103">Obtém dicas de camada de preços para atualizar um servidor de banco de dados do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="b979e-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="b979e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b979e-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b979e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b979e-105">DESCRIPTION</span></span>
<span data-ttu-id="b979e-106">O cmdlet **Get-AzSqlServerUpgradeHint** obtém dicas de camada de preços para atualizar um servidor de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b979e-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="b979e-107">As dicas podem conter o pool de banco de dados elástica e dicas de banco de dados autônomos.</span><span class="sxs-lookup"><span data-stu-id="b979e-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="b979e-108">Os bancos de dados que ainda estão em camadas de preços da Web e do Business têm uma dica para atualizar para as novas camadas de preços Básica, Padrão ou Premium ou para entrar no pool de banco de dados elástica.</span><span class="sxs-lookup"><span data-stu-id="b979e-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="b979e-109">Este cmdlet retorna dicas para todos os bancos de dados hospedados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="b979e-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="b979e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b979e-110">EXAMPLES</span></span>

### <span data-ttu-id="b979e-111">Exemplo 1: Obter recomendações combinadas</span><span class="sxs-lookup"><span data-stu-id="b979e-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="b979e-112">Este comando recebe recomendações combinadas para todos os bancos de dados em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="b979e-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="b979e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b979e-113">PARAMETERS</span></span>

### <span data-ttu-id="b979e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b979e-114">-DefaultProfile</span></span>
<span data-ttu-id="b979e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b979e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b979e-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="b979e-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="b979e-117">Indica se bancos de dados incluídos em pools de banco de dados elásticas devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b979e-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="b979e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b979e-118">-ResourceGroupName</span></span>
<span data-ttu-id="b979e-119">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="b979e-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b979e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b979e-120">-ServerName</span></span>
<span data-ttu-id="b979e-121">Especifica o nome do servidor para o qual este cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="b979e-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="b979e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b979e-122">-Confirm</span></span>
<span data-ttu-id="b979e-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b979e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b979e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b979e-124">-WhatIf</span></span>
<span data-ttu-id="b979e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b979e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b979e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b979e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b979e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b979e-127">CommonParameters</span></span>
<span data-ttu-id="b979e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b979e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b979e-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b979e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b979e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b979e-130">INPUTS</span></span>

### <span data-ttu-id="b979e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b979e-131">System.String</span></span>

### <span data-ttu-id="b979e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b979e-132">System.Boolean</span></span>

## <span data-ttu-id="b979e-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b979e-133">OUTPUTS</span></span>

### <span data-ttu-id="b979e-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="b979e-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="b979e-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="b979e-135">NOTES</span></span>

## <span data-ttu-id="b979e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b979e-136">RELATED LINKS</span></span>

[<span data-ttu-id="b979e-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b979e-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="b979e-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="b979e-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="b979e-139">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="b979e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


