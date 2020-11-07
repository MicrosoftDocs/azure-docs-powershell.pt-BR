---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: c07141d8a91974d511653217885b21a50a0b87f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773583"
---
# <span data-ttu-id="42432-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="42432-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="42432-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42432-102">SYNOPSIS</span></span>
<span data-ttu-id="42432-103">Failover de um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="42432-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="42432-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42432-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42432-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42432-105">DESCRIPTION</span></span>
<span data-ttu-id="42432-106">O cmdlet Invoke-AzSqlElasticPoolFailover se reserva um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="42432-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="42432-107">O failover ocorrerá em todos os bancos de dados no pool elástico após a execução desse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42432-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="42432-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42432-108">EXAMPLES</span></span>

### <span data-ttu-id="42432-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42432-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="42432-110">Esse comando fará o failover do pool elástico chamado "ElasticPool01" no servidor chamado "Server01".</span><span class="sxs-lookup"><span data-stu-id="42432-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="42432-111">Isso significa que o failover ocorrerá em todos os bancos de dados no pool elástico chamado "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="42432-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="42432-112">OS</span><span class="sxs-lookup"><span data-stu-id="42432-112">PARAMETERS</span></span>

### <span data-ttu-id="42432-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42432-113">-AsJob</span></span>
<span data-ttu-id="42432-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="42432-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42432-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42432-115">-DefaultProfile</span></span>
<span data-ttu-id="42432-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42432-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42432-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="42432-117">-ElasticPoolName</span></span>
<span data-ttu-id="42432-118">O nome do pool elástico do Azure SQL a ser removido.</span><span class="sxs-lookup"><span data-stu-id="42432-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="42432-119">-Force</span><span class="sxs-lookup"><span data-stu-id="42432-119">-Force</span></span>
<span data-ttu-id="42432-120">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="42432-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="42432-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42432-121">-PassThru</span></span>
<span data-ttu-id="42432-122">Na execução bem-sucedida, retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="42432-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="42432-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="42432-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42432-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42432-124">-ResourceGroupName</span></span>
<span data-ttu-id="42432-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42432-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="42432-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="42432-126">-ServerName</span></span>
<span data-ttu-id="42432-127">O nome do Azure SQL Server no qual o pool elástico está.</span><span class="sxs-lookup"><span data-stu-id="42432-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="42432-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42432-128">-Confirm</span></span>
<span data-ttu-id="42432-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42432-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42432-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42432-130">-WhatIf</span></span>
<span data-ttu-id="42432-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42432-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42432-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42432-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42432-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42432-133">CommonParameters</span></span>
<span data-ttu-id="42432-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42432-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42432-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42432-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42432-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42432-136">INPUTS</span></span>

### <span data-ttu-id="42432-137">System. String</span><span class="sxs-lookup"><span data-stu-id="42432-137">System.String</span></span>

## <span data-ttu-id="42432-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42432-138">OUTPUTS</span></span>

## <span data-ttu-id="42432-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42432-139">NOTES</span></span>

## <span data-ttu-id="42432-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42432-140">RELATED LINKS</span></span>

[<span data-ttu-id="42432-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="42432-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="42432-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="42432-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="42432-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="42432-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="42432-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="42432-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="42432-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="42432-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="42432-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="42432-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="42432-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="42432-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="42432-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="42432-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)