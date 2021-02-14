---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111306"
---
# <span data-ttu-id="b4a07-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4a07-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b4a07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4a07-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a07-103">Alterna um banco de dados secundário para ser principal para iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="b4a07-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="b4a07-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4a07-104">SYNTAX</span></span>

### <span data-ttu-id="b4a07-105">NoOptionsSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4a07-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a07-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="b4a07-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4a07-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4a07-107">DESCRIPTION</span></span>
<span data-ttu-id="b4a07-108">O cmdlet **Set-AzSqlDatabaseSecondary** alterna um banco de dados secundário para ser principal para iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="b4a07-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="b4a07-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado a iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="b4a07-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="b4a07-110">Especifique *o parâmetro AllowDataLoss* para iniciar um failover de força durante uma falha.</span><span class="sxs-lookup"><span data-stu-id="b4a07-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="b4a07-111">Você não precisa especificar esse parâmetro ao executar uma operação planejada, como uma busca drill de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b4a07-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="b4a07-112">No último caso, o banco de dados secundário é sincronizado com o principal antes de ser alternado.</span><span class="sxs-lookup"><span data-stu-id="b4a07-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="b4a07-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4a07-113">EXAMPLES</span></span>

### <span data-ttu-id="b4a07-114">Exemplo 1: Iniciar um failover planejado</span><span class="sxs-lookup"><span data-stu-id="b4a07-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="b4a07-115">Exemplo 2: Iniciar um failover forçado (com possível perda de dados)</span><span class="sxs-lookup"><span data-stu-id="b4a07-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="b4a07-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4a07-116">PARAMETERS</span></span>

### <span data-ttu-id="b4a07-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b4a07-117">-AllowDataLoss</span></span>
<span data-ttu-id="b4a07-118">Indica que essa operação de failover permite a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="b4a07-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="b4a07-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4a07-119">-AsJob</span></span>
<span data-ttu-id="b4a07-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4a07-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4a07-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="b4a07-121">-DatabaseName</span></span>
<span data-ttu-id="b4a07-122">Especifica o nome do Banco de Dados SQL do Azure Secundário.</span><span class="sxs-lookup"><span data-stu-id="b4a07-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b4a07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a07-123">-DefaultProfile</span></span>
<span data-ttu-id="b4a07-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b4a07-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4a07-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="b4a07-125">-Failover</span></span>
<span data-ttu-id="b4a07-126">Indica que esta operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="b4a07-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="b4a07-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a07-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b4a07-128">Especifica o nome do grupo de recursos ao qual o banco de dados SQL do Azure parceiro está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b4a07-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b4a07-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a07-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4a07-130">Especifica o nome do grupo de recursos ao qual o Banco de Dados SQL do Azure é atribuído.</span><span class="sxs-lookup"><span data-stu-id="b4a07-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="b4a07-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4a07-131">-ServerName</span></span>
<span data-ttu-id="b4a07-132">Especifica o nome do SQL Server que hospeda o Banco de Dados SQL do Azure Secundário.</span><span class="sxs-lookup"><span data-stu-id="b4a07-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b4a07-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4a07-133">-Confirm</span></span>
<span data-ttu-id="b4a07-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a07-135">-WhatIf</span></span>
<span data-ttu-id="b4a07-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4a07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a07-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4a07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a07-138">CommonParameters</span></span>
<span data-ttu-id="b4a07-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a07-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a07-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a07-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4a07-141">INPUTS</span></span>

### <span data-ttu-id="b4a07-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b4a07-142">System.String</span></span>

## <span data-ttu-id="b4a07-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4a07-143">OUTPUTS</span></span>

### <span data-ttu-id="b4a07-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b4a07-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b4a07-145">Notas</span><span class="sxs-lookup"><span data-stu-id="b4a07-145">NOTES</span></span>

## <span data-ttu-id="b4a07-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4a07-146">RELATED LINKS</span></span>

[<span data-ttu-id="b4a07-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4a07-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b4a07-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b4a07-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b4a07-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b4a07-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
