---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773855"
---
# <span data-ttu-id="5ae4e-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="5ae4e-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="5ae4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ae4e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae4e-103">Failover de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-103">Failovers a database.</span></span>

## <span data-ttu-id="5ae4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ae4e-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ae4e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ae4e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae4e-106">O cmdlet Invoke-AzSqlDatabaseFailover failover em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="5ae4e-107">Se o banco de dados estiver em um pool elástico, esse comando fará o failover do banco de dados fornecido sem afetar os outros bancos de dados no mesmo pool elástico.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="5ae4e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ae4e-108">EXAMPLES</span></span>

### <span data-ttu-id="5ae4e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ae4e-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5ae4e-110">Esse comando fará o failover do banco de dados chamado "Database01" no servidor chamado "Server01"</span><span class="sxs-lookup"><span data-stu-id="5ae4e-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="5ae4e-111">OS</span><span class="sxs-lookup"><span data-stu-id="5ae4e-111">PARAMETERS</span></span>

### <span data-ttu-id="5ae4e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ae4e-112">-AsJob</span></span>
<span data-ttu-id="5ae4e-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5ae4e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ae4e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ae4e-114">-DatabaseName</span></span>
<span data-ttu-id="5ae4e-115">O nome do banco de dados SQL do Azure para failover.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-115">The name of the Azure SQL Database to failover.</span></span>

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

### <span data-ttu-id="5ae4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae4e-116">-DefaultProfile</span></span>
<span data-ttu-id="5ae4e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ae4e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5ae4e-118">-Force</span></span>
<span data-ttu-id="5ae4e-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="5ae4e-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5ae4e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ae4e-120">-PassThru</span></span>
<span data-ttu-id="5ae4e-121">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="5ae4e-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ae4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ae4e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ae4e-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5ae4e-125">-ServerName</span></span>
<span data-ttu-id="5ae4e-126">O nome do servidor de banco de dados SQL do Azure no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="5ae4e-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ae4e-127">-Confirm</span></span>
<span data-ttu-id="5ae4e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ae4e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ae4e-129">-WhatIf</span></span>
<span data-ttu-id="5ae4e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ae4e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ae4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae4e-132">CommonParameters</span></span>
<span data-ttu-id="5ae4e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae4e-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ae4e-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae4e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ae4e-135">INPUTS</span></span>

### <span data-ttu-id="5ae4e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5ae4e-136">System.String</span></span>

## <span data-ttu-id="5ae4e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ae4e-137">OUTPUTS</span></span>

## <span data-ttu-id="5ae4e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ae4e-138">NOTES</span></span>

## <span data-ttu-id="5ae4e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ae4e-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ae4e-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="5ae4e-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="5ae4e-142">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-144">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-146">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ae4e-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5ae4e-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5ae4e-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
