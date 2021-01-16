---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426798"
---
# <span data-ttu-id="0103f-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="0103f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0103f-102">SYNOPSIS</span></span>
<span data-ttu-id="0103f-103">Modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0103f-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="0103f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0103f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0103f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0103f-105">DESCRIPTION</span></span>
<span data-ttu-id="0103f-106">Esse comando modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0103f-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="0103f-107">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="0103f-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="0103f-108">Para controlar o conjunto de bancos de dados no grupo, use "Add-AzSqlDatabaseToFailoverGroup" e "Remove-AzSqlDatabaseFromFailoverGroup" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0103f-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="0103f-109">Durante a visualização do recurso de grupos de failover, somente os valores maiores que ou iguais a 1 hora são compatíveis com o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="0103f-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="0103f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0103f-110">EXAMPLES</span></span>

### <span data-ttu-id="0103f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0103f-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="0103f-112">Define a política de failover do grupo de failover como ' automático '.</span><span class="sxs-lookup"><span data-stu-id="0103f-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="0103f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0103f-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="0103f-114">Define a política de failover do grupo de failover como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="0103f-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="0103f-115">OS</span><span class="sxs-lookup"><span data-stu-id="0103f-115">PARAMETERS</span></span>

### <span data-ttu-id="0103f-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="0103f-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="0103f-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0103f-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0103f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0103f-118">-DefaultProfile</span></span>
<span data-ttu-id="0103f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0103f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0103f-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="0103f-120">-FailoverGroupName</span></span>
<span data-ttu-id="0103f-121">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0103f-121">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0103f-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="0103f-122">-FailoverPolicy</span></span>
<span data-ttu-id="0103f-123">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0103f-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0103f-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="0103f-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="0103f-125">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="0103f-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="0103f-126">Isso indica que o banco de dados SQL do Azure não iniciará o failover automático antes do vencimento do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="0103f-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="0103f-127">Observe que a operação de failover com a opção AllowDataLoss pode causar perda de dados devido à natureza da sincronização assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0103f-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0103f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0103f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0103f-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0103f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0103f-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0103f-130">-ServerName</span></span>
<span data-ttu-id="0103f-131">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="0103f-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="0103f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0103f-132">CommonParameters</span></span>
<span data-ttu-id="0103f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0103f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0103f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0103f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0103f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0103f-135">INPUTS</span></span>

### <span data-ttu-id="0103f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0103f-136">System.String</span></span>

## <span data-ttu-id="0103f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0103f-137">OUTPUTS</span></span>

### <span data-ttu-id="0103f-138">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="0103f-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="0103f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0103f-139">NOTES</span></span>

## <span data-ttu-id="0103f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0103f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0103f-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0103f-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0103f-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="0103f-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="0103f-145">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0103f-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0103f-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="0103f-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0103f-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
