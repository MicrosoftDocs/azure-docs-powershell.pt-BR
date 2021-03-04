---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 9726d945b4e0fada340d06e780008f1921fb6f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890951"
---
# <span data-ttu-id="7626a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7626a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="7626a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7626a-102">SYNOPSIS</span></span>
<span data-ttu-id="7626a-103">Define uma política de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="7626a-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="7626a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7626a-104">SYNTAX</span></span>

### <span data-ttu-id="7626a-105">WeeklyRetentionRequired (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7626a-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7626a-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7626a-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7626a-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7626a-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7626a-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7626a-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7626a-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7626a-109">DESCRIPTION</span></span>
<span data-ttu-id="7626a-110">O cmdlet **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longo prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7626a-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="7626a-111">A política é um recurso de Backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="7626a-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="7626a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7626a-112">EXAMPLES</span></span>

### <span data-ttu-id="7626a-113">Exemplo 1: definir a retenção semanal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="7626a-114">Isso define a política de retenção de longo prazo do database01 para salvar cada backup completo semanal por 2 semanas</span><span class="sxs-lookup"><span data-stu-id="7626a-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="7626a-115">Exemplo 2: definir a retenção mensal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="7626a-116">Isso define a política de retenção de longo prazo do database01 para salvar o primeiro backup completo de cada mês por cinco anos</span><span class="sxs-lookup"><span data-stu-id="7626a-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="7626a-117">Exemplo 3: definir a retenção anual para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="7626a-118">Isso define a política de retenção de longo prazo do database01 para salvar o backup completo feito na 26ª semana do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="7626a-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="7626a-119">Exemplo 4: definir cada retenção para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="7626a-120">Isso define a política de retenção de longo prazo do database01 para salvar cada backup completo por 14 dias, o primeiro backup completo de cada mês por 24 semanas e o backup completo feito na 26ª semana do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="7626a-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="7626a-121">Exemplo 5: Remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="7626a-122">Remove a política do database01 para que ela não salve mais os backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7626a-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="7626a-123">Isso não afetará backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="7626a-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="7626a-124">Exemplo 6: Remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="7626a-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="7626a-125">Essa é outra maneira de remover a política para database01 para que ela não salve mais backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7626a-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="7626a-126">Isso não afetará backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="7626a-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="7626a-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7626a-127">PARAMETERS</span></span>

### <span data-ttu-id="7626a-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7626a-128">-DatabaseName</span></span>
<span data-ttu-id="7626a-129">O nome do banco de dados do Azure SQL a ser usado.</span><span class="sxs-lookup"><span data-stu-id="7626a-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="7626a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7626a-130">-DefaultProfile</span></span>
<span data-ttu-id="7626a-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7626a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7626a-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="7626a-132">-MonthlyRetention</span></span>
<span data-ttu-id="7626a-133">A Retenção Mensal.</span><span class="sxs-lookup"><span data-stu-id="7626a-133">The Monthly Retention.</span></span>
<span data-ttu-id="7626a-134">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão assumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7626a-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7626a-135">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7626a-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7626a-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7626a-136">-RemovePolicy</span></span>
<span data-ttu-id="7626a-137">Se fornecido, a política do banco de dados será removida.</span><span class="sxs-lookup"><span data-stu-id="7626a-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7626a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7626a-138">-ResourceGroupName</span></span>
<span data-ttu-id="7626a-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7626a-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="7626a-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7626a-140">-ServerName</span></span>
<span data-ttu-id="7626a-141">O nome do Azure SQL Server o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="7626a-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="7626a-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="7626a-142">-WeeklyRetention</span></span>
<span data-ttu-id="7626a-143">A Retenção Semanal.</span><span class="sxs-lookup"><span data-stu-id="7626a-143">The Weekly Retention.</span></span>
<span data-ttu-id="7626a-144">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão assumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7626a-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7626a-145">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7626a-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7626a-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="7626a-146">-WeekOfYear</span></span>
<span data-ttu-id="7626a-147">A Semana do Ano, de 1 a 52, a ser salva para a Retenção Anual.</span><span class="sxs-lookup"><span data-stu-id="7626a-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7626a-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="7626a-148">-YearlyRetention</span></span>
<span data-ttu-id="7626a-149">A Retenção Anual.</span><span class="sxs-lookup"><span data-stu-id="7626a-149">The Yearly Retention.</span></span>
<span data-ttu-id="7626a-150">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão assumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7626a-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7626a-151">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7626a-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7626a-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7626a-152">-Confirm</span></span>
<span data-ttu-id="7626a-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7626a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7626a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7626a-154">-WhatIf</span></span>
<span data-ttu-id="7626a-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7626a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7626a-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7626a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7626a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7626a-157">CommonParameters</span></span>
<span data-ttu-id="7626a-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7626a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7626a-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7626a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7626a-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7626a-160">INPUTS</span></span>

### <span data-ttu-id="7626a-161">System.String</span><span class="sxs-lookup"><span data-stu-id="7626a-161">System.String</span></span>

### <span data-ttu-id="7626a-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7626a-162">System.Int32</span></span>

## <span data-ttu-id="7626a-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7626a-163">OUTPUTS</span></span>

### <span data-ttu-id="7626a-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7626a-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="7626a-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="7626a-165">NOTES</span></span>

## <span data-ttu-id="7626a-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7626a-166">RELATED LINKS</span></span>

[<span data-ttu-id="7626a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7626a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7626a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7626a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7626a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7626a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7626a-170">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="7626a-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)