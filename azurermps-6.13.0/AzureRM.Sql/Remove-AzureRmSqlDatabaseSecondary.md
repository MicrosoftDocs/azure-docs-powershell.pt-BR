---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: f1bc8fcc019f25b4337dc88ac55965b8d988e753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431863"
---
# <span data-ttu-id="d9727-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d9727-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d9727-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9727-102">SYNOPSIS</span></span>
<span data-ttu-id="d9727-103">Finaliza a replicação de dados entre um banco de dados SQL e o banco de dados secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="d9727-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9727-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9727-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9727-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9727-105">DESCRIPTION</span></span>
<span data-ttu-id="d9727-106">O cmdlet **Remove-AzureRmSqlDatabaseSecondary** força a rescisão de um link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="d9727-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="d9727-107">Esse cmdlet substitui o cmdlet Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="d9727-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="d9727-108">Não há sincronização de duplicação antes do cancelamento.</span><span class="sxs-lookup"><span data-stu-id="d9727-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="d9727-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9727-109">EXAMPLES</span></span>

## <span data-ttu-id="d9727-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9727-110">PARAMETERS</span></span>

### <span data-ttu-id="d9727-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9727-111">-DatabaseName</span></span>
<span data-ttu-id="d9727-112">Especifica o nome do banco de dados SQL principal do Azure que tem o link de replicação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d9727-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9727-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9727-113">-DefaultProfile</span></span>
<span data-ttu-id="d9727-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d9727-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9727-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9727-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d9727-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="d9727-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="d9727-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d9727-117">-PartnerServerName</span></span>
<span data-ttu-id="d9727-118">Especifica o nome do SQL Server do parceiro.</span><span class="sxs-lookup"><span data-stu-id="d9727-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="d9727-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9727-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9727-120">Especifica o nome do grupo de recursos associado ao link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d9727-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="d9727-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d9727-121">-ServerName</span></span>
<span data-ttu-id="d9727-122">Especifica o nome do SQL Server que tem o link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d9727-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="d9727-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9727-123">-Confirm</span></span>
<span data-ttu-id="d9727-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9727-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9727-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9727-125">-WhatIf</span></span>
<span data-ttu-id="d9727-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9727-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9727-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9727-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9727-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9727-128">CommonParameters</span></span>
<span data-ttu-id="d9727-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9727-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9727-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9727-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9727-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9727-131">INPUTS</span></span>

### <span data-ttu-id="d9727-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d9727-132">System.String</span></span>

## <span data-ttu-id="d9727-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9727-133">OUTPUTS</span></span>

### <span data-ttu-id="d9727-134">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d9727-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d9727-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9727-135">NOTES</span></span>

## <span data-ttu-id="d9727-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9727-136">RELATED LINKS</span></span>

[<span data-ttu-id="d9727-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d9727-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d9727-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d9727-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d9727-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d9727-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
