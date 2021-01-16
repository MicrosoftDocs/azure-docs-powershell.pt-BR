---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263240"
---
# <span data-ttu-id="06de4-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="06de4-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="06de4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06de4-102">SYNOPSIS</span></span>
<span data-ttu-id="06de4-103">Failover de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="06de4-103">Failovers a database.</span></span>

## <span data-ttu-id="06de4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06de4-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06de4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06de4-105">DESCRIPTION</span></span>
<span data-ttu-id="06de4-106">O cmdlet Invoke-AzSqlDatabaseFailover failover em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="06de4-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="06de4-107">Se o banco de dados estiver em um pool elástico, esse comando fará o failover do banco de dados fornecido sem afetar os outros bancos de dados no mesmo pool elástico.</span><span class="sxs-lookup"><span data-stu-id="06de4-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="06de4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06de4-108">EXAMPLES</span></span>

### <span data-ttu-id="06de4-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06de4-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="06de4-110">Esse comando fará o failover da réplica primária do banco de dados chamada "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="06de4-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="06de4-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06de4-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="06de4-112">Esse comando fará o failover da réplica secundária legível do banco de dados chamada "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="06de4-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="06de4-113">OS</span><span class="sxs-lookup"><span data-stu-id="06de4-113">PARAMETERS</span></span>

### <span data-ttu-id="06de4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06de4-114">-AsJob</span></span>
<span data-ttu-id="06de4-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="06de4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06de4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06de4-116">-DatabaseName</span></span>
<span data-ttu-id="06de4-117">O nome do banco de dados SQL do Azure para failover.</span><span class="sxs-lookup"><span data-stu-id="06de4-117">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="06de4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06de4-118">-DefaultProfile</span></span>
<span data-ttu-id="06de4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06de4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06de4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="06de4-120">-Force</span></span>
<span data-ttu-id="06de4-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="06de4-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="06de4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06de4-122">-PassThru</span></span>
<span data-ttu-id="06de4-123">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="06de4-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="06de4-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="06de4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06de4-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="06de4-125">-ReadableSecondary</span></span>
<span data-ttu-id="06de4-126">Failover da réplica secundária legível em vez da réplica primária padrão</span><span class="sxs-lookup"><span data-stu-id="06de4-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="06de4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06de4-127">-ResourceGroupName</span></span>
<span data-ttu-id="06de4-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06de4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="06de4-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="06de4-129">-ServerName</span></span>
<span data-ttu-id="06de4-130">O nome do servidor de banco de dados SQL do Azure no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="06de4-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="06de4-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06de4-131">-Confirm</span></span>
<span data-ttu-id="06de4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06de4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06de4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06de4-133">-WhatIf</span></span>
<span data-ttu-id="06de4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06de4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06de4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06de4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06de4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06de4-136">CommonParameters</span></span>
<span data-ttu-id="06de4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06de4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06de4-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06de4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06de4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06de4-139">INPUTS</span></span>

### <span data-ttu-id="06de4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="06de4-140">System.String</span></span>

## <span data-ttu-id="06de4-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06de4-141">OUTPUTS</span></span>

## <span data-ttu-id="06de4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06de4-142">NOTES</span></span>

## <span data-ttu-id="06de4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06de4-143">RELATED LINKS</span></span>

[<span data-ttu-id="06de4-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="06de4-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="06de4-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="06de4-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="06de4-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="06de4-148">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="06de4-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="06de4-150">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06de4-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="06de4-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="06de4-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
