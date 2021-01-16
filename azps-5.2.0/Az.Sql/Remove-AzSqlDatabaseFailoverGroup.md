---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261541"
---
# <span data-ttu-id="4f5eb-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4f5eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5eb-103">Remove um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4f5eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f5eb-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f5eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f5eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5eb-106">Esse comando Remove o grupo de failover com o nome especificado, deixando todos os bancos de dados e relações de replicação intactos.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="4f5eb-107">O ponto de extremidade de escuta será cancelado do DNS.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="4f5eb-108">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="4f5eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f5eb-109">EXAMPLES</span></span>

### <span data-ttu-id="4f5eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f5eb-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4f5eb-111">Remover um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="4f5eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="4f5eb-112">PARAMETERS</span></span>

### <span data-ttu-id="4f5eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5eb-113">-DefaultProfile</span></span>
<span data-ttu-id="4f5eb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f5eb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f5eb-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5eb-115">-FailoverGroupName</span></span>
<span data-ttu-id="4f5eb-116">O nome do grupo de failover de banco de dados SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="4f5eb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f5eb-117">-Force</span></span>
<span data-ttu-id="4f5eb-118">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4f5eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f5eb-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f5eb-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4f5eb-121">-ServerName</span></span>
<span data-ttu-id="4f5eb-122">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4f5eb-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4f5eb-123">-Confirm</span></span>
<span data-ttu-id="4f5eb-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f5eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f5eb-125">-WhatIf</span></span>
<span data-ttu-id="4f5eb-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f5eb-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f5eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5eb-128">CommonParameters</span></span>
<span data-ttu-id="4f5eb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5eb-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f5eb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5eb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f5eb-131">INPUTS</span></span>

### <span data-ttu-id="4f5eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4f5eb-132">System.String</span></span>

## <span data-ttu-id="4f5eb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f5eb-133">OUTPUTS</span></span>

### <span data-ttu-id="4f5eb-134">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4f5eb-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4f5eb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f5eb-135">NOTES</span></span>

## <span data-ttu-id="4f5eb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f5eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="4f5eb-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f5eb-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f5eb-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f5eb-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4f5eb-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4f5eb-142">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4f5eb-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4f5eb-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4f5eb-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
