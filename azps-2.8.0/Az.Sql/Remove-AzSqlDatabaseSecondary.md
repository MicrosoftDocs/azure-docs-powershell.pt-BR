---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 6e77f70c92d9075671a0011e54c4cc4fc5df764c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773548"
---
# <span data-ttu-id="d8ab9-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d8ab9-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d8ab9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ab9-103">Finaliza a replicação de dados entre um banco de dados SQL e o banco de dados secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="d8ab9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8ab9-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ab9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8ab9-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ab9-106">O cmdlet **Remove-AzSqlDatabaseSecondary** força a rescisão de um link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="d8ab9-107">Esse cmdlet substitui o cmdlet Stop-AzSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="d8ab9-108">Não há sincronização de duplicação antes do cancelamento.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="d8ab9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8ab9-109">EXAMPLES</span></span>

## <span data-ttu-id="d8ab9-110">OS</span><span class="sxs-lookup"><span data-stu-id="d8ab9-110">PARAMETERS</span></span>

### <span data-ttu-id="d8ab9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8ab9-111">-DatabaseName</span></span>
<span data-ttu-id="d8ab9-112">Especifica o nome do banco de dados SQL principal do Azure que tem o link de replicação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8ab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ab9-113">-DefaultProfile</span></span>
<span data-ttu-id="d8ab9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d8ab9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8ab9-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ab9-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d8ab9-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="d8ab9-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d8ab9-117">-PartnerServerName</span></span>
<span data-ttu-id="d8ab9-118">Especifica o nome do SQL Server do parceiro.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="d8ab9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ab9-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8ab9-120">Especifica o nome do grupo de recursos associado ao link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="d8ab9-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d8ab9-121">-ServerName</span></span>
<span data-ttu-id="d8ab9-122">Especifica o nome do SQL Server que tem o link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="d8ab9-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8ab9-123">-Confirm</span></span>
<span data-ttu-id="d8ab9-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ab9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ab9-125">-WhatIf</span></span>
<span data-ttu-id="d8ab9-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ab9-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ab9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ab9-128">CommonParameters</span></span>
<span data-ttu-id="d8ab9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ab9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ab9-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8ab9-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ab9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8ab9-131">INPUTS</span></span>

### <span data-ttu-id="d8ab9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ab9-132">System.String</span></span>

## <span data-ttu-id="d8ab9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8ab9-133">OUTPUTS</span></span>

### <span data-ttu-id="d8ab9-134">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d8ab9-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d8ab9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8ab9-135">NOTES</span></span>

## <span data-ttu-id="d8ab9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8ab9-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8ab9-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d8ab9-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d8ab9-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d8ab9-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d8ab9-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8ab9-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
