---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 3462a22c793679632e4bf0a559530c4ea1becf3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598925"
---
# <span data-ttu-id="355fe-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="355fe-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="355fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="355fe-102">SYNOPSIS</span></span>
<span data-ttu-id="355fe-103">Obtém dicas de camada de preço para atualizar um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="355fe-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="355fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="355fe-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="355fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="355fe-105">DESCRIPTION</span></span>
<span data-ttu-id="355fe-106">O cmdlet **Get-AzSqlServerUpgradeHint** Obtém dicas de camada de preços para a atualização de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="355fe-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="355fe-107">As dicas podem conter o pool de banco de dados elástico e as dicas de banco de dados autônomos.</span><span class="sxs-lookup"><span data-stu-id="355fe-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="355fe-108">Os bancos de dados que ainda estão nas faixas de preços da Web e de negócios recebem uma dica para fazer a atualização para as novas camadas de preço básico, padrão ou Premium ou para acessar o pool de banco de dados elástico.</span><span class="sxs-lookup"><span data-stu-id="355fe-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="355fe-109">Esse cmdlet retorna dicas para todos os bancos de dados hospedados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="355fe-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="355fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="355fe-110">EXAMPLES</span></span>

### <span data-ttu-id="355fe-111">Exemplo 1: obter recomendações combinadas</span><span class="sxs-lookup"><span data-stu-id="355fe-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="355fe-112">Esse comando obtém recomendações combinadas para todos os bancos de dados em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="355fe-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="355fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="355fe-113">PARAMETERS</span></span>

### <span data-ttu-id="355fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="355fe-114">-DefaultProfile</span></span>
<span data-ttu-id="355fe-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="355fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="355fe-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="355fe-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="355fe-117">Indica se os bancos de dados incluídos em pools de bancos de dados elásticos devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="355fe-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="355fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="355fe-119">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="355fe-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="355fe-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="355fe-120">-ServerName</span></span>
<span data-ttu-id="355fe-121">Especifica o nome do servidor para o qual esse cmdlet obtém uma dica de atualização.</span><span class="sxs-lookup"><span data-stu-id="355fe-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="355fe-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="355fe-122">-Confirm</span></span>
<span data-ttu-id="355fe-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="355fe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="355fe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="355fe-124">-WhatIf</span></span>
<span data-ttu-id="355fe-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="355fe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="355fe-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="355fe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="355fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="355fe-127">CommonParameters</span></span>
<span data-ttu-id="355fe-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="355fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="355fe-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="355fe-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="355fe-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="355fe-130">INPUTS</span></span>

### <span data-ttu-id="355fe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="355fe-131">System.String</span></span>

### <span data-ttu-id="355fe-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="355fe-132">System.Boolean</span></span>

## <span data-ttu-id="355fe-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="355fe-133">OUTPUTS</span></span>

### <span data-ttu-id="355fe-134">Microsoft. Azure. Commands. Sql. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="355fe-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="355fe-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="355fe-135">NOTES</span></span>

## <span data-ttu-id="355fe-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="355fe-136">RELATED LINKS</span></span>

[<span data-ttu-id="355fe-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="355fe-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="355fe-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="355fe-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="355fe-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="355fe-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


