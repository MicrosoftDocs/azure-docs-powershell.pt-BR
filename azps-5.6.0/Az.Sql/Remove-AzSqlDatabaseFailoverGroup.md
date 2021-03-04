---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886559"
---
# <span data-ttu-id="176d6-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="176d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176d6-102">SYNOPSIS</span></span>
<span data-ttu-id="176d6-103">Remove um Grupo de Failover SQL Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="176d6-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="176d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="176d6-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="176d6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="176d6-105">DESCRIPTION</span></span>
<span data-ttu-id="176d6-106">Este comando remove o Grupo de Failover com o nome especificado, deixando todos os bancos de dados e relações de replicação intactas.</span><span class="sxs-lookup"><span data-stu-id="176d6-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="176d6-107">O ponto de extremidade do ouvinte será não registro no DNS.</span><span class="sxs-lookup"><span data-stu-id="176d6-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="176d6-108">O servidor principal do Grupo de Failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="176d6-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="176d6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="176d6-109">EXAMPLES</span></span>

### <span data-ttu-id="176d6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="176d6-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="176d6-111">Remover um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="176d6-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="176d6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="176d6-112">PARAMETERS</span></span>

### <span data-ttu-id="176d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176d6-113">-DefaultProfile</span></span>
<span data-ttu-id="176d6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="176d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="176d6-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="176d6-115">-FailoverGroupName</span></span>
<span data-ttu-id="176d6-116">O nome do Grupo de Failover SQL banco de dados do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="176d6-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="176d6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="176d6-117">-Force</span></span>
<span data-ttu-id="176d6-118">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="176d6-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="176d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="176d6-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="176d6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="176d6-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="176d6-121">-ServerName</span></span>
<span data-ttu-id="176d6-122">O nome do Servidor de Banco de Dados do Azure SQL principal do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="176d6-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="176d6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176d6-123">-Confirm</span></span>
<span data-ttu-id="176d6-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176d6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176d6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176d6-125">-WhatIf</span></span>
<span data-ttu-id="176d6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="176d6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176d6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="176d6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176d6-128">CommonParameters</span></span>
<span data-ttu-id="176d6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176d6-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="176d6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176d6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="176d6-131">INPUTS</span></span>

### <span data-ttu-id="176d6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="176d6-132">System.String</span></span>

## <span data-ttu-id="176d6-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="176d6-133">OUTPUTS</span></span>

### <span data-ttu-id="176d6-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="176d6-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="176d6-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="176d6-135">NOTES</span></span>

## <span data-ttu-id="176d6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="176d6-136">RELATED LINKS</span></span>

[<span data-ttu-id="176d6-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="176d6-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="176d6-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="176d6-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="176d6-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="176d6-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="176d6-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="176d6-143">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="176d6-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
