---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 708b010a8ff7b2a289d538a07e7b679fcec6efab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610042"
---
# <span data-ttu-id="337ca-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="337ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="337ca-102">SYNOPSIS</span></span>
<span data-ttu-id="337ca-103">Executa um failover de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="337ca-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="337ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="337ca-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="337ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="337ca-105">DESCRIPTION</span></span>
<span data-ttu-id="337ca-106">Esse comando troca as funções dos servidores em um grupo de failover e alterna todos os bancos de dados secundários para a função primária.</span><span class="sxs-lookup"><span data-stu-id="337ca-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="337ca-107">Todas as novas sessões TDS são automaticamente redirecionadas para o servidor secundário após a atualização do cache do cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="337ca-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="337ca-108">Quando o servidor primário original estiver novamente online, todos os bancos de dados primários anteriormente serão alternados para a função secundária.</span><span class="sxs-lookup"><span data-stu-id="337ca-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="337ca-109">O servidor secundário do grupo de failover deve ser usado para executar este comando.</span><span class="sxs-lookup"><span data-stu-id="337ca-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="337ca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="337ca-110">EXAMPLES</span></span>

### <span data-ttu-id="337ca-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="337ca-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="337ca-112">Emita uma operação de failover que permita a perda de dados por meio do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="337ca-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="337ca-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="337ca-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="337ca-114">Emita uma melhor operação de failover de esforço que será bem-sucedida sem perder dados ou falhar e reverter.</span><span class="sxs-lookup"><span data-stu-id="337ca-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="337ca-115">OS</span><span class="sxs-lookup"><span data-stu-id="337ca-115">PARAMETERS</span></span>

### <span data-ttu-id="337ca-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="337ca-116">-AllowDataLoss</span></span>
<span data-ttu-id="337ca-117">Conclua o failover mesmo se fizer isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="337ca-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="337ca-118">Isso permitirá que o failover prossiga mesmo se um banco de dados primário estiver indisponível.</span><span class="sxs-lookup"><span data-stu-id="337ca-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337ca-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="337ca-119">-AsJob</span></span>
<span data-ttu-id="337ca-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="337ca-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="337ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337ca-121">-DefaultProfile</span></span>
<span data-ttu-id="337ca-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="337ca-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="337ca-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="337ca-123">-FailoverGroupName</span></span>
<span data-ttu-id="337ca-124">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="337ca-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="337ca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337ca-125">-ResourceGroupName</span></span>
<span data-ttu-id="337ca-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="337ca-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="337ca-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="337ca-127">-ServerName</span></span>
<span data-ttu-id="337ca-128">O nome do servidor de banco de dados SQL do Azure secundário do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="337ca-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="337ca-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="337ca-129">-Confirm</span></span>
<span data-ttu-id="337ca-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="337ca-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337ca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337ca-131">-WhatIf</span></span>
<span data-ttu-id="337ca-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="337ca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="337ca-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="337ca-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337ca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337ca-134">CommonParameters</span></span>
<span data-ttu-id="337ca-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337ca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337ca-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337ca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337ca-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="337ca-137">INPUTS</span></span>

### <span data-ttu-id="337ca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="337ca-138">System.String</span></span>

## <span data-ttu-id="337ca-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="337ca-139">OUTPUTS</span></span>

### <span data-ttu-id="337ca-140">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="337ca-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="337ca-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="337ca-141">NOTES</span></span>

## <span data-ttu-id="337ca-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="337ca-142">RELATED LINKS</span></span>

[<span data-ttu-id="337ca-143">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="337ca-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="337ca-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="337ca-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="337ca-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="337ca-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="337ca-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="337ca-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="337ca-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
