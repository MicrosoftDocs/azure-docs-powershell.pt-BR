---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 98a6ceafed2c7c62301c63ff1c8b3028c46e1201
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428343"
---
# <span data-ttu-id="1fb06-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="1fb06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fb06-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb06-103">Modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb06-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fb06-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fb06-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb06-106">Esse comando modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb06-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="1fb06-107">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="1fb06-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="1fb06-108">Para controlar o conjunto de bancos de dados no grupo, use "Add-AzureRmSqlDatabaseToFailoverGroup" e "Remove-AzureRmSqlDatabaseFromFailoverGroup" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1fb06-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="1fb06-109">Durante a visualização do recurso de grupos de failover, somente os valores maiores que ou iguais a 1 hora são compatíveis com o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="1fb06-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1fb06-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fb06-110">EXAMPLES</span></span>

### <span data-ttu-id="1fb06-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fb06-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="1fb06-112">Define a política de failover do grupo de failover como ' automático '.</span><span class="sxs-lookup"><span data-stu-id="1fb06-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="1fb06-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1fb06-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="1fb06-114">Define a política de failover do grupo de failover como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="1fb06-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="1fb06-115">OS</span><span class="sxs-lookup"><span data-stu-id="1fb06-115">PARAMETERS</span></span>

### <span data-ttu-id="1fb06-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1fb06-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1fb06-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1fb06-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="1fb06-118">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1fb06-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="1fb06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb06-119">-DefaultProfile</span></span>
<span data-ttu-id="1fb06-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1fb06-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fb06-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb06-121">-FailoverGroupName</span></span>
<span data-ttu-id="1fb06-122">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb06-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="1fb06-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb06-123">-FailoverPolicy</span></span>
<span data-ttu-id="1fb06-124">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb06-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="1fb06-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1fb06-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1fb06-126">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="1fb06-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="1fb06-127">Isso indica que o banco de dados SQL do Azure não iniciará o failover automático antes do vencimento do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="1fb06-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="1fb06-128">Observe que a operação de failover com a opção AllowDataLoss pode causar perda de dados devido à natureza da sincronização assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1fb06-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="1fb06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb06-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fb06-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb06-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fb06-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1fb06-131">-ServerName</span></span>
<span data-ttu-id="1fb06-132">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="1fb06-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="1fb06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb06-133">CommonParameters</span></span>
<span data-ttu-id="1fb06-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb06-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb06-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb06-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fb06-136">INPUTS</span></span>

### <span data-ttu-id="1fb06-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb06-137">System.String</span></span>

## <span data-ttu-id="1fb06-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fb06-138">OUTPUTS</span></span>

### <span data-ttu-id="1fb06-139">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1fb06-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="1fb06-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fb06-140">NOTES</span></span>

## <span data-ttu-id="1fb06-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fb06-141">RELATED LINKS</span></span>

[<span data-ttu-id="1fb06-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1fb06-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1fb06-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="1fb06-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="1fb06-146">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1fb06-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fb06-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1fb06-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="1fb06-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
