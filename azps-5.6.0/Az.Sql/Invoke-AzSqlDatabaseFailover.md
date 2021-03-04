---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 23df8f00c91cfabf4ad01b5dd641069f159eb064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889885"
---
# <span data-ttu-id="6e80f-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="6e80f-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="6e80f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e80f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e80f-103">Failovers um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6e80f-103">Failovers a database.</span></span>

## <span data-ttu-id="6e80f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e80f-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e80f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e80f-105">DESCRIPTION</span></span>
<span data-ttu-id="6e80f-106">O Invoke-AzSqlDatabaseFailover cmdlet de falha em um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6e80f-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="6e80f-107">Se o banco de dados estiver em um pool elástica, esse comando fará failover no banco de dados determinado sem afetar os outros bancos de dados no mesmo pool elástica.</span><span class="sxs-lookup"><span data-stu-id="6e80f-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="6e80f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e80f-108">EXAMPLES</span></span>

### <span data-ttu-id="6e80f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e80f-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="6e80f-110">Este comando fará failover da réplica principal do banco de dados chamado "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="6e80f-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="6e80f-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e80f-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="6e80f-112">Este comando fará failover da réplica secundária acessível do banco de dados chamado "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="6e80f-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="6e80f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e80f-113">PARAMETERS</span></span>

### <span data-ttu-id="6e80f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e80f-114">-AsJob</span></span>
<span data-ttu-id="6e80f-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6e80f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e80f-116">-DatabaseName</span></span>
<span data-ttu-id="6e80f-117">O nome do banco de dados do Azure SQL failover.</span><span class="sxs-lookup"><span data-stu-id="6e80f-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e80f-118">-DefaultProfile</span></span>
<span data-ttu-id="6e80f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e80f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e80f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e80f-120">-Force</span></span>
<span data-ttu-id="6e80f-121">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="6e80f-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e80f-122">-PassThru</span></span>
<span data-ttu-id="6e80f-123">Em Execução bem-sucedida, retorna true.</span><span class="sxs-lookup"><span data-stu-id="6e80f-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="6e80f-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6e80f-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6e80f-125">-ReadableSecondary</span></span>
<span data-ttu-id="6e80f-126">Failover da réplica secundária acessível em vez da réplica primária padrão</span><span class="sxs-lookup"><span data-stu-id="6e80f-126">Failover the readable secondary replica instead of the default primary replica</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e80f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e80f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e80f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e80f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e80f-129">-ServerName</span></span>
<span data-ttu-id="6e80f-130">O nome do Servidor de Banco de Dados do Azure SQL em que o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="6e80f-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="6e80f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e80f-131">-Confirm</span></span>
<span data-ttu-id="6e80f-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e80f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e80f-133">-WhatIf</span></span>
<span data-ttu-id="6e80f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e80f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e80f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e80f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e80f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e80f-136">CommonParameters</span></span>
<span data-ttu-id="6e80f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e80f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e80f-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e80f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e80f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e80f-139">INPUTS</span></span>

### <span data-ttu-id="6e80f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6e80f-140">System.String</span></span>

## <span data-ttu-id="6e80f-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e80f-141">OUTPUTS</span></span>

## <span data-ttu-id="6e80f-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e80f-142">NOTES</span></span>

## <span data-ttu-id="6e80f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e80f-143">RELATED LINKS</span></span>

[<span data-ttu-id="6e80f-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="6e80f-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="6e80f-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6e80f-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="6e80f-151">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="6e80f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
