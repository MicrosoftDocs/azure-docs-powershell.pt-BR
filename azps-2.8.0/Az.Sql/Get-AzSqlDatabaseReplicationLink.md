---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773662"
---
# <span data-ttu-id="41a6d-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="41a6d-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="41a6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="41a6d-103">Obtém os links de replicação geográfica entre um banco de dados SQL do Azure e um grupo de recursos ou um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="41a6d-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="41a6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41a6d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="41a6d-106">O cmdlet **Get-AzSqlDatabaseReplicationLink** substitui o cmdlet **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="41a6d-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="41a6d-107">Ele obtém todos os links de replicação geográfica entre o banco de dados SQL do Azure especificado e um grupo de recursos ou AzureSQL Server.</span><span class="sxs-lookup"><span data-stu-id="41a6d-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="41a6d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41a6d-108">EXAMPLES</span></span>

## <span data-ttu-id="41a6d-109">OS</span><span class="sxs-lookup"><span data-stu-id="41a6d-109">PARAMETERS</span></span>

### <span data-ttu-id="41a6d-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41a6d-110">-DatabaseName</span></span>
<span data-ttu-id="41a6d-111">Especifica o nome do banco de dados SQL para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="41a6d-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="41a6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a6d-112">-DefaultProfile</span></span>
<span data-ttu-id="41a6d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="41a6d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41a6d-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a6d-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="41a6d-115">Especifica o nome do grupo de recursos ao qual o parceiro está atribuído.</span><span class="sxs-lookup"><span data-stu-id="41a6d-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="41a6d-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="41a6d-116">-PartnerServerName</span></span>
<span data-ttu-id="41a6d-117">Especifica o nome do Azure SQL Server para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="41a6d-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="41a6d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a6d-118">-ResourceGroupName</span></span>
<span data-ttu-id="41a6d-119">Especifica o nome do grupo de recursos do Azure para o banco de dados para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="41a6d-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="41a6d-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="41a6d-120">-ServerName</span></span>
<span data-ttu-id="41a6d-121">Especifica o nome do SQL Server para o banco de dados para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="41a6d-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="41a6d-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41a6d-122">-Confirm</span></span>
<span data-ttu-id="41a6d-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41a6d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a6d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a6d-124">-WhatIf</span></span>
<span data-ttu-id="41a6d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41a6d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41a6d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41a6d-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a6d-127">CommonParameters</span></span>
<span data-ttu-id="41a6d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a6d-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41a6d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a6d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41a6d-130">INPUTS</span></span>

### <span data-ttu-id="41a6d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="41a6d-131">System.String</span></span>

## <span data-ttu-id="41a6d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41a6d-132">OUTPUTS</span></span>

### <span data-ttu-id="41a6d-133">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="41a6d-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="41a6d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41a6d-134">NOTES</span></span>

## <span data-ttu-id="41a6d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41a6d-135">RELATED LINKS</span></span>

[<span data-ttu-id="41a6d-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="41a6d-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)