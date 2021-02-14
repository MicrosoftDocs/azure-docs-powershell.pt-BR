---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117083"
---
# <span data-ttu-id="15b19-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="15b19-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="15b19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15b19-102">SYNOPSIS</span></span>
<span data-ttu-id="15b19-103">Falha em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="15b19-103">Failovers a database.</span></span>

## <span data-ttu-id="15b19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15b19-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b19-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="15b19-105">DESCRIPTION</span></span>
<span data-ttu-id="15b19-106">O Invoke-AzSqlDatabaseFailover cmdlet failovers de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="15b19-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="15b19-107">Se o banco de dados estiver em um pool elástica, esse comando fará failover no banco de dados determinado sem afetar os outros bancos de dados no mesmo pool elástica.</span><span class="sxs-lookup"><span data-stu-id="15b19-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="15b19-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15b19-108">EXAMPLES</span></span>

### <span data-ttu-id="15b19-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15b19-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="15b19-110">Esse comando fará failover na réplica principal do banco de dados chamado "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="15b19-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="15b19-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="15b19-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="15b19-112">Esse comando fará failover a réplica secundária acessível do banco de dados chamado "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="15b19-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="15b19-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15b19-113">PARAMETERS</span></span>

### <span data-ttu-id="15b19-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15b19-114">-AsJob</span></span>
<span data-ttu-id="15b19-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="15b19-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15b19-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="15b19-116">-DatabaseName</span></span>
<span data-ttu-id="15b19-117">O nome do banco de dados SQL do Azure para failover.</span><span class="sxs-lookup"><span data-stu-id="15b19-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="15b19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b19-118">-DefaultProfile</span></span>
<span data-ttu-id="15b19-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15b19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15b19-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="15b19-120">-Force</span></span>
<span data-ttu-id="15b19-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="15b19-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="15b19-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15b19-122">-PassThru</span></span>
<span data-ttu-id="15b19-123">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="15b19-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="15b19-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="15b19-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15b19-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="15b19-125">-ReadableSecondary</span></span>
<span data-ttu-id="15b19-126">Failover a replica secundária acessível em vez da replica primária padrão</span><span class="sxs-lookup"><span data-stu-id="15b19-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="15b19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b19-127">-ResourceGroupName</span></span>
<span data-ttu-id="15b19-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15b19-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="15b19-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15b19-129">-ServerName</span></span>
<span data-ttu-id="15b19-130">O nome do Servidor de Banco de Dados SQL do Azure no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="15b19-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="15b19-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="15b19-131">-Confirm</span></span>
<span data-ttu-id="15b19-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b19-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b19-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b19-133">-WhatIf</span></span>
<span data-ttu-id="15b19-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="15b19-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15b19-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15b19-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b19-136">CommonParameters</span></span>
<span data-ttu-id="15b19-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b19-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15b19-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b19-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="15b19-139">INPUTS</span></span>

### <span data-ttu-id="15b19-140">System.String</span><span class="sxs-lookup"><span data-stu-id="15b19-140">System.String</span></span>

## <span data-ttu-id="15b19-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="15b19-141">OUTPUTS</span></span>

## <span data-ttu-id="15b19-142">Notas</span><span class="sxs-lookup"><span data-stu-id="15b19-142">NOTES</span></span>

## <span data-ttu-id="15b19-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15b19-143">RELATED LINKS</span></span>

[<span data-ttu-id="15b19-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="15b19-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="15b19-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="15b19-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="15b19-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="15b19-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="15b19-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="15b19-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="15b19-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="15b19-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="15b19-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
