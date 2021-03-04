---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886557"
---
# <span data-ttu-id="2f165-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2f165-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="2f165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f165-102">SYNOPSIS</span></span>
<span data-ttu-id="2f165-103">Encerra a replicação de dados entre um banco de dados SQL e o banco de dados secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="2f165-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="2f165-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2f165-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f165-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2f165-105">DESCRIPTION</span></span>
<span data-ttu-id="2f165-106">O cmdlet **Remove-AzSqlDatabaseSecondary** força o término de um link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="2f165-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="2f165-107">Este cmdlet substitui o Stop-AzSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f165-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="2f165-108">Não há sincronização de replicação antes do término.</span><span class="sxs-lookup"><span data-stu-id="2f165-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="2f165-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f165-109">EXAMPLES</span></span>

## <span data-ttu-id="2f165-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2f165-110">PARAMETERS</span></span>

### <span data-ttu-id="2f165-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f165-111">-DatabaseName</span></span>
<span data-ttu-id="2f165-112">Especifica o nome do banco de dados primário do Azure SQL que tem o link de replicação que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="2f165-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f165-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f165-113">-DefaultProfile</span></span>
<span data-ttu-id="2f165-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2f165-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f165-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f165-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2f165-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="2f165-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f165-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2f165-117">-PartnerServerName</span></span>
<span data-ttu-id="2f165-118">Especifica o nome do parceiro SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f165-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f165-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f165-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f165-120">Especifica o nome do grupo de recursos associado ao link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2f165-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="2f165-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f165-121">-ServerName</span></span>
<span data-ttu-id="2f165-122">Especifica o nome da SQL Server que tem o link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2f165-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="2f165-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f165-123">-Confirm</span></span>
<span data-ttu-id="2f165-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f165-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f165-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f165-125">-WhatIf</span></span>
<span data-ttu-id="2f165-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f165-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f165-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f165-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f165-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f165-128">CommonParameters</span></span>
<span data-ttu-id="2f165-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f165-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f165-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f165-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f165-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f165-131">INPUTS</span></span>

### <span data-ttu-id="2f165-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2f165-132">System.String</span></span>

## <span data-ttu-id="2f165-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2f165-133">OUTPUTS</span></span>

### <span data-ttu-id="2f165-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="2f165-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="2f165-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="2f165-135">NOTES</span></span>

## <span data-ttu-id="2f165-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f165-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f165-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2f165-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="2f165-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2f165-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="2f165-139">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="2f165-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
