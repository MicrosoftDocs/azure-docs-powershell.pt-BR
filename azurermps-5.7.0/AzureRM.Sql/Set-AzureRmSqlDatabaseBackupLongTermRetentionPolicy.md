---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c5450ea3ffdcc8c76fa88c8721902b8f8ae77794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428706"
---
# <span data-ttu-id="bd6ad-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd6ad-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="bd6ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="bd6ad-103">Define uma política de retenção de longo prazo do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd6ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd6ad-104">SYNTAX</span></span>

### <span data-ttu-id="bd6ad-105">WeeklyRetentionRequired (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd6ad-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ad-106">Herança</span><span class="sxs-lookup"><span data-stu-id="bd6ad-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ad-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="bd6ad-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ad-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="bd6ad-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>] [-MonthlyRetention] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd6ad-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="bd6ad-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>]
 [[-MonthlyRetention] <String>] [-YearlyRetention] <String> [-WeekOfYear] <Int32> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd6ad-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd6ad-110">DESCRIPTION</span></span>
<span data-ttu-id="bd6ad-111">O cmdlet **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longo prazo registrada para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="bd6ad-112">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="bd6ad-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd6ad-113">EXAMPLES</span></span>

### <span data-ttu-id="bd6ad-114">Exemplo 1: definir a retenção semanal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-115">Isso define a política de retenção de longo prazo do database01 para salvar cada backup semanal completo por duas semanas</span><span class="sxs-lookup"><span data-stu-id="bd6ad-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="bd6ad-116">Exemplo 2: definir a retenção mensal para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-117">Isso define a política de retenção de longo prazo do database01 para salvar o primeiro backup completo de cada mês durante 5 anos</span><span class="sxs-lookup"><span data-stu-id="bd6ad-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="bd6ad-118">Exemplo 3: definir a retenção anual para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-119">Isso define a política de retenção de longo prazo do database01 para salvar o backup completo realizado na semana 26th do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="bd6ad-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="bd6ad-120">Exemplo 4: definir cada retenção para a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-121">Isso define a política de retenção de longo prazo do database01 para salvar cada backup completo por 14 dias, o primeiro backup completo de cada mês por 24 semanas, e o backup completo realizado na semana 26th do ano por 10 anos</span><span class="sxs-lookup"><span data-stu-id="bd6ad-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="bd6ad-122">Exemplo 4: remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-123">Remove a política para database01, portanto, não salva mais nenhum backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="bd6ad-124">Isso não afetará os backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="bd6ad-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="bd6ad-125">Exemplo 4: remover a política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="bd6ad-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="bd6ad-126">Essa é outra maneira de remover a política do database01 para que ela não salve mais nenhum backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="bd6ad-127">Isso não afetará os backups que já foram feitos</span><span class="sxs-lookup"><span data-stu-id="bd6ad-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="bd6ad-128">OS</span><span class="sxs-lookup"><span data-stu-id="bd6ad-128">PARAMETERS</span></span>

### <span data-ttu-id="bd6ad-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd6ad-129">-DatabaseName</span></span>
<span data-ttu-id="bd6ad-130">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-130">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd6ad-131">-DefaultProfile</span></span>
<span data-ttu-id="bd6ad-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="bd6ad-133">-MonthlyRetention</span></span>
<span data-ttu-id="bd6ad-134">A retenção mensal.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-134">The Monthly Retention.</span></span>
<span data-ttu-id="bd6ad-135">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="bd6ad-136">Há um minumum de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="bd6ad-137">-RemovePolicy</span></span>
<span data-ttu-id="bd6ad-138">Se fornecido, a política para o banco de dados será removida.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd6ad-139">-ResourceGroupName</span></span>
<span data-ttu-id="bd6ad-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-140">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd6ad-141">-ResourceId</span></span>
<span data-ttu-id="bd6ad-142">A ID do recurso da política de retenção de longo prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-143">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bd6ad-143">-ServerName</span></span>
<span data-ttu-id="bd6ad-144">O nome do Azure SQL Server no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-144">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-145">-Estado</span><span class="sxs-lookup"><span data-stu-id="bd6ad-145">-State</span></span>
<span data-ttu-id="bd6ad-146">O estado da política de backup de retenção de longo prazo, ' habilitado ' ou ' desabilitado '</span><span class="sxs-lookup"><span data-stu-id="bd6ad-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="bd6ad-147">-WeeklyRetention</span></span>
<span data-ttu-id="bd6ad-148">A retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-148">The Weekly Retention.</span></span>
<span data-ttu-id="bd6ad-149">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="bd6ad-150">Há um minumum de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="bd6ad-151">-WeekOfYear</span></span>
<span data-ttu-id="bd6ad-152">A semana do ano, de 1 a 52, para economizar pela retenção anual.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="bd6ad-153">-YearlyRetention</span></span>
<span data-ttu-id="bd6ad-154">A retenção anual.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-154">The Yearly Retention.</span></span>
<span data-ttu-id="bd6ad-155">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="bd6ad-156">Há um minumum de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd6ad-157">-Confirm</span></span>
<span data-ttu-id="bd6ad-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd6ad-159">-WhatIf</span></span>
<span data-ttu-id="bd6ad-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd6ad-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd6ad-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd6ad-162">CommonParameters</span></span>
<span data-ttu-id="bd6ad-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd6ad-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd6ad-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd6ad-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd6ad-165">INPUTS</span></span>

### <span data-ttu-id="bd6ad-166">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bd6ad-166">None</span></span>
<span data-ttu-id="bd6ad-167">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bd6ad-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd6ad-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd6ad-168">OUTPUTS</span></span>

### <span data-ttu-id="bd6ad-169">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bd6ad-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="bd6ad-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd6ad-170">NOTES</span></span>

## <span data-ttu-id="bd6ad-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd6ad-171">RELATED LINKS</span></span>

[<span data-ttu-id="bd6ad-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd6ad-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="bd6ad-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bd6ad-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="bd6ad-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bd6ad-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="bd6ad-175">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="bd6ad-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
