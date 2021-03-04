---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888603"
---
# <span data-ttu-id="e7e21-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="e7e21-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="e7e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e21-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e21-103">Failovers um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="e7e21-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="e7e21-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7e21-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7e21-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7e21-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e21-106">O Invoke-AzSqlElasticPoolFailover cmdlet faz failovers em um pool elástica.</span><span class="sxs-lookup"><span data-stu-id="e7e21-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="e7e21-107">O failover ocorrerá em todos os bancos de dados no pool elástica após a execução deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7e21-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="e7e21-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7e21-108">EXAMPLES</span></span>

### <span data-ttu-id="e7e21-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7e21-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e7e21-110">Este comando fará failover no pool elástica chamado "ElasticPool01" no servidor chamado "Server01".</span><span class="sxs-lookup"><span data-stu-id="e7e21-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="e7e21-111">Isso significa que o failover ocorrerá em todos os bancos de dados no pool elástica chamado "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="e7e21-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="e7e21-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7e21-112">PARAMETERS</span></span>

### <span data-ttu-id="e7e21-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7e21-113">-AsJob</span></span>
<span data-ttu-id="e7e21-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e7e21-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7e21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e21-115">-DefaultProfile</span></span>
<span data-ttu-id="e7e21-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7e21-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e7e21-117">-ElasticPoolName</span></span>
<span data-ttu-id="e7e21-118">O nome do Pool SQL Elastic do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e7e21-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="e7e21-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e7e21-119">-Force</span></span>
<span data-ttu-id="e7e21-120">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="e7e21-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e7e21-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7e21-121">-PassThru</span></span>
<span data-ttu-id="e7e21-122">Em Execução bem-sucedida, retorna true.</span><span class="sxs-lookup"><span data-stu-id="e7e21-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="e7e21-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e7e21-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7e21-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e21-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7e21-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7e21-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7e21-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7e21-126">-ServerName</span></span>
<span data-ttu-id="e7e21-127">O nome do Azure SQL Server pool elástica está.</span><span class="sxs-lookup"><span data-stu-id="e7e21-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="e7e21-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7e21-128">-Confirm</span></span>
<span data-ttu-id="e7e21-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7e21-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7e21-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7e21-130">-WhatIf</span></span>
<span data-ttu-id="e7e21-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7e21-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7e21-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7e21-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7e21-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e21-133">CommonParameters</span></span>
<span data-ttu-id="e7e21-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e21-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e21-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7e21-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e21-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7e21-136">INPUTS</span></span>

### <span data-ttu-id="e7e21-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e21-137">System.String</span></span>

## <span data-ttu-id="e7e21-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7e21-138">OUTPUTS</span></span>

## <span data-ttu-id="e7e21-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7e21-139">NOTES</span></span>

## <span data-ttu-id="e7e21-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7e21-140">RELATED LINKS</span></span>

[<span data-ttu-id="e7e21-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e7e21-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="e7e21-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e7e21-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="e7e21-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="e7e21-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="e7e21-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="e7e21-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="e7e21-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e7e21-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e7e21-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e7e21-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="e7e21-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e7e21-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="e7e21-148">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="e7e21-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)