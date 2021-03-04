---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 7b23bd6082fc79ff6096f496117c0ff6b63fd134
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887321"
---
# <span data-ttu-id="d2812-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d2812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2812-102">SYNOPSIS</span></span>
<span data-ttu-id="d2812-103">Obtém ou lista grupos de failover do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="d2812-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="d2812-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2812-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2812-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2812-105">DESCRIPTION</span></span>
<span data-ttu-id="d2812-106">Obtém um grupo de failover de banco de dados específico do Azure SQL ou lista os Grupos de Failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="d2812-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="d2812-107">Qualquer servidor no Grupo de Failover pode ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="d2812-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="d2812-108">Os valores retornados refletirão o estado do servidor especificado em relação ao Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="d2812-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="d2812-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2812-109">EXAMPLES</span></span>

### <span data-ttu-id="d2812-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2812-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="d2812-111">Lista todos os Grupos de Failover em um servidor.</span><span class="sxs-lookup"><span data-stu-id="d2812-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="d2812-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2812-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="d2812-113">Obter um Grupo de Failover específico.</span><span class="sxs-lookup"><span data-stu-id="d2812-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="d2812-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d2812-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="d2812-115">Obter todos os grupos de failover em um servidor que comece com "fg".</span><span class="sxs-lookup"><span data-stu-id="d2812-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="d2812-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2812-116">PARAMETERS</span></span>

### <span data-ttu-id="d2812-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2812-117">-DefaultProfile</span></span>
<span data-ttu-id="d2812-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d2812-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2812-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d2812-119">-FailoverGroupName</span></span>
<span data-ttu-id="d2812-120">O nome do Grupo de Failover SQL banco de dados do Azure a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="d2812-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2812-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2812-121">-ResourceGroupName</span></span>
<span data-ttu-id="d2812-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2812-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2812-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2812-123">-ServerName</span></span>
<span data-ttu-id="d2812-124">O nome do Servidor de Banco de Dados do Azure SQL do qual recuperar o Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="d2812-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="d2812-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2812-125">CommonParameters</span></span>
<span data-ttu-id="d2812-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2812-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2812-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2812-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2812-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2812-128">INPUTS</span></span>

### <span data-ttu-id="d2812-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d2812-129">System.String</span></span>

## <span data-ttu-id="d2812-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2812-130">OUTPUTS</span></span>

### <span data-ttu-id="d2812-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d2812-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d2812-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2812-132">NOTES</span></span>

## <span data-ttu-id="d2812-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2812-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2812-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d2812-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d2812-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d2812-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d2812-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d2812-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d2812-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d2812-140">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d2812-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
