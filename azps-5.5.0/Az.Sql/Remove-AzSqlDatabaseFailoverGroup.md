---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110929"
---
# <span data-ttu-id="f9f1d-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f9f1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f1d-103">Remove um Grupo de Failover de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f9f1d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9f1d-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9f1d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f1d-106">Esse comando remove o Grupo de Failover com o nome especificado, deixando todos os bancos de dados e relações de replicação intactos.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="f9f1d-107">O ponto de extremidade do ouvinte será não registro do DNS.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="f9f1d-108">O servidor principal do Grupo de Failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="f9f1d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="f9f1d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9f1d-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="f9f1d-111">Remover um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="f9f1d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9f1d-112">PARAMETERS</span></span>

### <span data-ttu-id="f9f1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f1d-113">-DefaultProfile</span></span>
<span data-ttu-id="f9f1d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f9f1d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9f1d-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f1d-115">-FailoverGroupName</span></span>
<span data-ttu-id="f9f1d-116">O nome do Grupo de Failover do Banco de Dados SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="f9f1d-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f9f1d-117">-Force</span></span>
<span data-ttu-id="f9f1d-118">Ignorar a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="f9f1d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f1d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9f1d-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9f1d-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9f1d-121">-ServerName</span></span>
<span data-ttu-id="f9f1d-122">O nome do servidor de banco de dados SQL principal do Azure do Grupo failover.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f9f1d-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f9f1d-123">-Confirm</span></span>
<span data-ttu-id="f9f1d-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f1d-125">-WhatIf</span></span>
<span data-ttu-id="f9f1d-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f1d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f1d-128">CommonParameters</span></span>
<span data-ttu-id="f9f1d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f1d-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9f1d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f1d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9f1d-131">INPUTS</span></span>

### <span data-ttu-id="f9f1d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9f1d-132">System.String</span></span>

## <span data-ttu-id="f9f1d-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9f1d-133">OUTPUTS</span></span>

### <span data-ttu-id="f9f1d-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f9f1d-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f9f1d-135">Notas</span><span class="sxs-lookup"><span data-stu-id="f9f1d-135">NOTES</span></span>

## <span data-ttu-id="f9f1d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9f1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="f9f1d-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f9f1d-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f9f1d-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f9f1d-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f9f1d-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f9f1d-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f9f1d-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f9f1d-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f9f1d-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
