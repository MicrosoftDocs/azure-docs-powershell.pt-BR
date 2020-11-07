---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 825d6f367fb4fbace53fccdb8798d17a915fc2bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778044"
---
# <span data-ttu-id="de755-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="de755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de755-102">SYNOPSIS</span></span>
<span data-ttu-id="de755-103">Modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="de755-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="de755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de755-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de755-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de755-105">DESCRIPTION</span></span>
<span data-ttu-id="de755-106">Esse comando modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="de755-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="de755-107">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="de755-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="de755-108">Para controlar o conjunto de bancos de dados no grupo, use "Add-AzSqlDatabaseToFailoverGroup" e "Remove-AzSqlDatabaseFromFailoverGroup" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="de755-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="de755-109">Durante a visualização do recurso de grupos de failover, somente os valores maiores que ou iguais a 1 hora são compatíveis com o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="de755-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="de755-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de755-110">EXAMPLES</span></span>

### <span data-ttu-id="de755-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de755-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="de755-112">Define a política de failover do grupo de failover como ' automático '.</span><span class="sxs-lookup"><span data-stu-id="de755-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="de755-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de755-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="de755-114">Define a política de failover do grupo de failover como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="de755-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="de755-115">OS</span><span class="sxs-lookup"><span data-stu-id="de755-115">PARAMETERS</span></span>

### <span data-ttu-id="de755-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="de755-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="de755-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="de755-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="de755-118">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="de755-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="de755-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de755-119">-DefaultProfile</span></span>
<span data-ttu-id="de755-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="de755-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de755-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="de755-121">-FailoverGroupName</span></span>
<span data-ttu-id="de755-122">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="de755-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="de755-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="de755-123">-FailoverPolicy</span></span>
<span data-ttu-id="de755-124">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="de755-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="de755-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="de755-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="de755-126">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="de755-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="de755-127">Isso indica que o banco de dados SQL do Azure não iniciará o failover automático antes do vencimento do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="de755-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="de755-128">Observe que a operação de failover com a opção AllowDataLoss pode causar perda de dados devido à natureza da sincronização assíncrona.</span><span class="sxs-lookup"><span data-stu-id="de755-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="de755-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de755-129">-ResourceGroupName</span></span>
<span data-ttu-id="de755-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de755-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="de755-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="de755-131">-ServerName</span></span>
<span data-ttu-id="de755-132">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="de755-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="de755-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de755-133">CommonParameters</span></span>
<span data-ttu-id="de755-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de755-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de755-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de755-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de755-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de755-136">INPUTS</span></span>

### <span data-ttu-id="de755-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de755-137">System.String</span></span>

## <span data-ttu-id="de755-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de755-138">OUTPUTS</span></span>

### <span data-ttu-id="de755-139">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="de755-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="de755-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de755-140">NOTES</span></span>

## <span data-ttu-id="de755-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de755-141">RELATED LINKS</span></span>

[<span data-ttu-id="de755-142">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-142">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de755-143">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-143">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de755-144">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-144">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="de755-145">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-145">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="de755-146">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-146">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de755-147">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="de755-147">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="de755-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="de755-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
