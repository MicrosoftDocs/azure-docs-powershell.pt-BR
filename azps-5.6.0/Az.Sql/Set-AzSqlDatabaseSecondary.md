---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: fc0a6bc7fa87a78fedd0416ea1578b9404168dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887297"
---
# <span data-ttu-id="f6110-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6110-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f6110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6110-102">SYNOPSIS</span></span>
<span data-ttu-id="f6110-103">Alterna um banco de dados secundário para ser principal para iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="f6110-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="f6110-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6110-104">SYNTAX</span></span>

### <span data-ttu-id="f6110-105">NoOptionsSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6110-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6110-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="f6110-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6110-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6110-107">DESCRIPTION</span></span>
<span data-ttu-id="f6110-108">O cmdlet **Set-AzSqlDatabaseSecondary** alterna um banco de dados secundário para ser principal para iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="f6110-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="f6110-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado a iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="f6110-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="f6110-110">Especifique *o parâmetro AllowDataLoss* para iniciar um failover de força durante uma paralisação.</span><span class="sxs-lookup"><span data-stu-id="f6110-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="f6110-111">Você não precisa especificar esse parâmetro quando executar uma operação planejada, como a broca de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f6110-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="f6110-112">No último caso, o banco de dados secundário é sincronizado com o principal antes de ser comutado.</span><span class="sxs-lookup"><span data-stu-id="f6110-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="f6110-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6110-113">EXAMPLES</span></span>

### <span data-ttu-id="f6110-114">Exemplo 1: Iniciar um failover planejado</span><span class="sxs-lookup"><span data-stu-id="f6110-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="f6110-115">Exemplo 2: Iniciar um failover forçado (com perda potencial de dados)</span><span class="sxs-lookup"><span data-stu-id="f6110-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="f6110-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6110-116">PARAMETERS</span></span>

### <span data-ttu-id="f6110-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f6110-117">-AllowDataLoss</span></span>
<span data-ttu-id="f6110-118">Indica que essa operação de failover permite a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="f6110-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6110-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6110-119">-AsJob</span></span>
<span data-ttu-id="f6110-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f6110-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6110-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6110-121">-DatabaseName</span></span>
<span data-ttu-id="f6110-122">Especifica o nome do Banco de Dados do Azure SQL Secundário.</span><span class="sxs-lookup"><span data-stu-id="f6110-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="f6110-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6110-123">-DefaultProfile</span></span>
<span data-ttu-id="f6110-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f6110-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6110-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="f6110-125">-Failover</span></span>
<span data-ttu-id="f6110-126">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="f6110-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6110-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6110-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f6110-128">Especifica o nome do grupo de recursos ao qual o banco de dados do Azure SQL parceiro é atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6110-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="f6110-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6110-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6110-130">Especifica o nome do grupo de recursos ao qual o Azure SQL Banco de Dados Secundário é atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6110-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="f6110-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6110-131">-ServerName</span></span>
<span data-ttu-id="f6110-132">Especifica o nome do SQL Server que hospeda o Banco de Dados secundário do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="f6110-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="f6110-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6110-133">-Confirm</span></span>
<span data-ttu-id="f6110-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6110-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6110-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6110-135">-WhatIf</span></span>
<span data-ttu-id="f6110-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6110-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6110-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6110-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6110-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6110-138">CommonParameters</span></span>
<span data-ttu-id="f6110-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6110-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6110-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6110-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6110-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6110-141">INPUTS</span></span>

### <span data-ttu-id="f6110-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f6110-142">System.String</span></span>

## <span data-ttu-id="f6110-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6110-143">OUTPUTS</span></span>

### <span data-ttu-id="f6110-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f6110-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f6110-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6110-145">NOTES</span></span>

## <span data-ttu-id="f6110-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6110-146">RELATED LINKS</span></span>

[<span data-ttu-id="f6110-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6110-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f6110-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6110-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f6110-149">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f6110-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
