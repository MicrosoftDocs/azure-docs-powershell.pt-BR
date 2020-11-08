---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124742"
---
# <span data-ttu-id="3bb6d-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3bb6d-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="3bb6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb6d-103">Define uma política de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="3bb6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bb6d-104">SYNTAX</span></span>

### <span data-ttu-id="3bb6d-105">WeeklyRetentionRequired (padrão)</span><span class="sxs-lookup"><span data-stu-id="3bb6d-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb6d-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="3bb6d-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bb6d-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="3bb6d-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb6d-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="3bb6d-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bb6d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3bb6d-109">DESCRIPTION</span></span>
<span data-ttu-id="3bb6d-110">O cmdlet **set-AzSqlDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longo prazo registrada para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="3bb6d-111">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="3bb6d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3bb6d-112">EXAMPLES</span></span>

### <span data-ttu-id="3bb6d-113">Exemplo 1: definir a retenção semanal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-114">Isso define a política de retenção de longo prazo do database01 para salvar cada backup semanal completo por duas semanas</span><span class="sxs-lookup"><span data-stu-id="3bb6d-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="3bb6d-115">Exemplo 2: definir a retenção mensal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-116">Isso define a política de retenção de longo prazo do database01 para salvar o primeiro backup completo de cada mês durante 5 anos</span><span class="sxs-lookup"><span data-stu-id="3bb6d-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="3bb6d-117">Exemplo 3: definir a retenção anual para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-118">Isso define a política de retenção de longo prazo do database01 para salvar o backup completo realizado na semana 26th do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="3bb6d-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="3bb6d-119">Exemplo 4: definir cada retenção para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-120">Isso define a política de retenção de longo prazo do database01 para salvar cada backup completo por 14 dias, o primeiro backup completo de cada mês por 24 semanas, e o backup completo realizado na semana 26th do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="3bb6d-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="3bb6d-121">Exemplo 5: remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-122">Remove a política para database01, portanto, não salva mais nenhum backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="3bb6d-123">Isso não afetará os backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="3bb6d-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="3bb6d-124">Exemplo 6: remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="3bb6d-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="3bb6d-125">Essa é outra maneira de remover a política do database01 para que ela não salve mais nenhum backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="3bb6d-126">Isso não afetará os backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="3bb6d-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="3bb6d-127">OS</span><span class="sxs-lookup"><span data-stu-id="3bb6d-127">PARAMETERS</span></span>

### <span data-ttu-id="3bb6d-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3bb6d-128">-DatabaseName</span></span>
<span data-ttu-id="3bb6d-129">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="3bb6d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb6d-130">-DefaultProfile</span></span>
<span data-ttu-id="3bb6d-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb6d-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="3bb6d-132">-MonthlyRetention</span></span>
<span data-ttu-id="3bb6d-133">A retenção mensal.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-133">The Monthly Retention.</span></span>
<span data-ttu-id="3bb6d-134">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3bb6d-135">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="3bb6d-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="3bb6d-136">-RemovePolicy</span></span>
<span data-ttu-id="3bb6d-137">Se fornecido, a política para o banco de dados será removida.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="3bb6d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb6d-138">-ResourceGroupName</span></span>
<span data-ttu-id="3bb6d-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="3bb6d-140">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3bb6d-140">-ServerName</span></span>
<span data-ttu-id="3bb6d-141">O nome do Azure SQL Server no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="3bb6d-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="3bb6d-142">-WeeklyRetention</span></span>
<span data-ttu-id="3bb6d-143">A retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-143">The Weekly Retention.</span></span>
<span data-ttu-id="3bb6d-144">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3bb6d-145">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="3bb6d-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="3bb6d-146">-WeekOfYear</span></span>
<span data-ttu-id="3bb6d-147">A semana do ano, de 1 a 52, para economizar pela retenção anual.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="3bb6d-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="3bb6d-148">-YearlyRetention</span></span>
<span data-ttu-id="3bb6d-149">A retenção anual.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-149">The Yearly Retention.</span></span>
<span data-ttu-id="3bb6d-150">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="3bb6d-151">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="3bb6d-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3bb6d-152">-Confirm</span></span>
<span data-ttu-id="3bb6d-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb6d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb6d-154">-WhatIf</span></span>
<span data-ttu-id="3bb6d-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb6d-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb6d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb6d-157">CommonParameters</span></span>
<span data-ttu-id="3bb6d-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb6d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb6d-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb6d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb6d-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3bb6d-160">INPUTS</span></span>

### <span data-ttu-id="3bb6d-161">System. String</span><span class="sxs-lookup"><span data-stu-id="3bb6d-161">System.String</span></span>

### <span data-ttu-id="3bb6d-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3bb6d-162">System.Int32</span></span>

## <span data-ttu-id="3bb6d-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3bb6d-163">OUTPUTS</span></span>

### <span data-ttu-id="3bb6d-164">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3bb6d-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3bb6d-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3bb6d-165">NOTES</span></span>

## <span data-ttu-id="3bb6d-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bb6d-166">RELATED LINKS</span></span>

[<span data-ttu-id="3bb6d-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3bb6d-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3bb6d-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3bb6d-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3bb6d-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3bb6d-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3bb6d-170">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3bb6d-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)