---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110903"
---
# <span data-ttu-id="d8ee0-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ee0-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d8ee0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ee0-103">O cmdlet **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** define a política de retenção de longo prazo de um banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="d8ee0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8ee0-104">SYNTAX</span></span>

### <span data-ttu-id="d8ee0-105">WeeklyRetentionRequired (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8ee0-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ee0-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="d8ee0-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ee0-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="d8ee0-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ee0-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="d8ee0-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8ee0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8ee0-109">DESCRIPTION</span></span>
<span data-ttu-id="d8ee0-110">O cmdlet **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longo prazo para esse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="d8ee0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8ee0-111">EXAMPLES</span></span>

### <span data-ttu-id="d8ee0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8ee0-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="d8ee0-113">Configura a política semanal de retenção de longo prazo do banco de dados para uma semana.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="d8ee0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d8ee0-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="d8ee0-115">Esse comando remove a política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="d8ee0-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d8ee0-116">Example 3</span></span>

<span data-ttu-id="d8ee0-117">O Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet define a política de retenção de longo prazo de um banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="d8ee0-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d8ee0-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="d8ee0-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8ee0-119">PARAMETERS</span></span>

### <span data-ttu-id="d8ee0-120">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="d8ee0-120">-DatabaseName</span></span>
<span data-ttu-id="d8ee0-121">O nome do Banco de Dados Gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="d8ee0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ee0-122">-DefaultProfile</span></span>
<span data-ttu-id="d8ee0-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ee0-124">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="d8ee0-124">-InstanceName</span></span>
<span data-ttu-id="d8ee0-125">O nome da Instância Gerenciada do Azure ao banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="d8ee0-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="d8ee0-126">-MonthlyRetention</span></span>
<span data-ttu-id="d8ee0-127">A Retenção Mensal.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-127">The Monthly Retention.</span></span>
<span data-ttu-id="d8ee0-128">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão presumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d8ee0-129">Há no mínimo sete dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d8ee0-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="d8ee0-130">-RemovePolicy</span></span>
<span data-ttu-id="d8ee0-131">Se fornecido, a política do banco de dados será des limpa.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="d8ee0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ee0-132">-ResourceGroupName</span></span>
<span data-ttu-id="d8ee0-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8ee0-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="d8ee0-134">-WeeklyRetention</span></span>
<span data-ttu-id="d8ee0-135">A Retenção Semanal.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-135">The Weekly Retention.</span></span>
<span data-ttu-id="d8ee0-136">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão presumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d8ee0-137">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d8ee0-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="d8ee0-138">-WeekOfYear</span></span>
<span data-ttu-id="d8ee0-139">A Semana do Ano, de 1 a 52, a ser salva para a Retenção Anual.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="d8ee0-140">-AnualRetention</span><span class="sxs-lookup"><span data-stu-id="d8ee0-140">-YearlyRetention</span></span>
<span data-ttu-id="d8ee0-141">A Retenção Anual.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-141">The Yearly Retention.</span></span>
<span data-ttu-id="d8ee0-142">Se apenas um número for passado em vez de uma cadeia de caracteres ISO 8601, os dias serão presumidos como as unidades.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="d8ee0-143">Há no mínimo sete dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="d8ee0-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d8ee0-144">-Confirm</span></span>
<span data-ttu-id="d8ee0-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ee0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ee0-146">-WhatIf</span></span>
<span data-ttu-id="d8ee0-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ee0-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ee0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ee0-149">CommonParameters</span></span>
<span data-ttu-id="d8ee0-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ee0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ee0-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8ee0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ee0-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8ee0-152">INPUTS</span></span>

### <span data-ttu-id="d8ee0-153">System.String</span><span class="sxs-lookup"><span data-stu-id="d8ee0-153">System.String</span></span>

### <span data-ttu-id="d8ee0-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d8ee0-154">System.Int32</span></span>

## <span data-ttu-id="d8ee0-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8ee0-155">OUTPUTS</span></span>

### <span data-ttu-id="d8ee0-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d8ee0-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d8ee0-157">Notas</span><span class="sxs-lookup"><span data-stu-id="d8ee0-157">NOTES</span></span>

## <span data-ttu-id="d8ee0-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8ee0-158">RELATED LINKS</span></span>

[<span data-ttu-id="d8ee0-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8ee0-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d8ee0-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d8ee0-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d8ee0-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d8ee0-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d8ee0-162">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8ee0-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)