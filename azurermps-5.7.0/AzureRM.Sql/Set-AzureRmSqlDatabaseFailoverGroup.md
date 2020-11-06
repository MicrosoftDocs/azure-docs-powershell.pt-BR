---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428701"
---
# <span data-ttu-id="fdf2a-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="fdf2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdf2a-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf2a-103">Modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdf2a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdf2a-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf2a-106">Esse comando modifica a configuração de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="fdf2a-107">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="fdf2a-108">Para controlar o conjunto de bancos de dados no grupo, use "Add-AzureRmSqlDatabaseToFailoverGroup" e "Remove-AzureRmSqlDatabaseFromFailoverGroup" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="fdf2a-109">Durante a visualização do recurso de grupos de failover, somente os valores maiores que ou iguais a 1 hora são compatíveis com o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="fdf2a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdf2a-110">EXAMPLES</span></span>

### <span data-ttu-id="fdf2a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdf2a-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="fdf2a-112">Define a política de failover do grupo de failover como ' automático '.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="fdf2a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fdf2a-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="fdf2a-114">Define a política de failover do grupo de failover como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="fdf2a-115">OS</span><span class="sxs-lookup"><span data-stu-id="fdf2a-115">PARAMETERS</span></span>

### <span data-ttu-id="fdf2a-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="fdf2a-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="fdf2a-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="fdf2a-118">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf2a-119">-DefaultProfile</span></span>
<span data-ttu-id="fdf2a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fdf2a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf2a-121">-FailoverGroupName</span></span>
<span data-ttu-id="fdf2a-122">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="fdf2a-123">-FailoverPolicy</span></span>
<span data-ttu-id="fdf2a-124">A política de failover do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="fdf2a-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="fdf2a-126">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="fdf2a-127">Isso indica que o banco de dados SQL do Azure não iniciará o failover automático antes do vencimento do período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="fdf2a-128">Observe que a operação de failover com a opção AllowDataLoss pode causar perda de dados devido à natureza da sincronização assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf2a-129">-ResourceGroupName</span></span>
<span data-ttu-id="fdf2a-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fdf2a-131">-ServerName</span></span>
<span data-ttu-id="fdf2a-132">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf2a-133">CommonParameters</span></span>
<span data-ttu-id="fdf2a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf2a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf2a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf2a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdf2a-136">INPUTS</span></span>

### <span data-ttu-id="fdf2a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf2a-137">System.String</span></span>

## <span data-ttu-id="fdf2a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdf2a-138">OUTPUTS</span></span>

### <span data-ttu-id="fdf2a-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="fdf2a-139">System.Object</span></span>

## <span data-ttu-id="fdf2a-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdf2a-140">NOTES</span></span>

## <span data-ttu-id="fdf2a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdf2a-141">RELATED LINKS</span></span>

[<span data-ttu-id="fdf2a-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdf2a-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdf2a-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="fdf2a-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="fdf2a-146">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdf2a-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2a-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="fdf2a-148">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fdf2a-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
