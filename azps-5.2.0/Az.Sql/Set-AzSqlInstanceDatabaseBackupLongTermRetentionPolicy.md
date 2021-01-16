---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260458"
---
# <span data-ttu-id="71216-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71216-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="71216-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71216-102">SYNOPSIS</span></span>
<span data-ttu-id="71216-103">O cmdlet **set-AzSqlInstanceDatabaseLongTermRetentionBackup** define a política de retenção de longo prazo do banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="71216-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="71216-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71216-104">SYNTAX</span></span>

### <span data-ttu-id="71216-105">WeeklyRetentionRequired (padrão)</span><span class="sxs-lookup"><span data-stu-id="71216-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71216-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="71216-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71216-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="71216-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71216-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="71216-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71216-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71216-109">DESCRIPTION</span></span>
<span data-ttu-id="71216-110">O cmdlet **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longa duração para esse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="71216-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="71216-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71216-111">EXAMPLES</span></span>

### <span data-ttu-id="71216-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71216-112">Example 1</span></span>
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

<span data-ttu-id="71216-113">Configura a política semanal de retenção de longo prazo do banco de dados para uma semana.</span><span class="sxs-lookup"><span data-stu-id="71216-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="71216-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="71216-114">Example 2</span></span>
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

<span data-ttu-id="71216-115">Esse comando Remove a política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71216-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="71216-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="71216-116">Example 3</span></span>

<span data-ttu-id="71216-117">O cmdlet Set-AzSqlInstanceDatabaseLongTermRetentionBackup define a política de retenção de longo prazo de um banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="71216-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="71216-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="71216-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="71216-119">OS</span><span class="sxs-lookup"><span data-stu-id="71216-119">PARAMETERS</span></span>

### <span data-ttu-id="71216-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71216-120">-DatabaseName</span></span>
<span data-ttu-id="71216-121">O nome do banco de dados gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="71216-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="71216-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71216-122">-DefaultProfile</span></span>
<span data-ttu-id="71216-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71216-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71216-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="71216-124">-InstanceName</span></span>
<span data-ttu-id="71216-125">O nome da instância gerenciada do Azure à qual o banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="71216-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="71216-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="71216-126">-MonthlyRetention</span></span>
<span data-ttu-id="71216-127">A retenção mensal.</span><span class="sxs-lookup"><span data-stu-id="71216-127">The Monthly Retention.</span></span>
<span data-ttu-id="71216-128">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="71216-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="71216-129">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="71216-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="71216-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="71216-130">-RemovePolicy</span></span>
<span data-ttu-id="71216-131">Se fornecido, a política para o banco de dados será limpa.</span><span class="sxs-lookup"><span data-stu-id="71216-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="71216-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71216-132">-ResourceGroupName</span></span>
<span data-ttu-id="71216-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71216-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="71216-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="71216-134">-WeeklyRetention</span></span>
<span data-ttu-id="71216-135">A retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="71216-135">The Weekly Retention.</span></span>
<span data-ttu-id="71216-136">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="71216-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="71216-137">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="71216-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="71216-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="71216-138">-WeekOfYear</span></span>
<span data-ttu-id="71216-139">A semana do ano, de 1 a 52, para economizar pela retenção anual.</span><span class="sxs-lookup"><span data-stu-id="71216-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="71216-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="71216-140">-YearlyRetention</span></span>
<span data-ttu-id="71216-141">A retenção anual.</span><span class="sxs-lookup"><span data-stu-id="71216-141">The Yearly Retention.</span></span>
<span data-ttu-id="71216-142">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="71216-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="71216-143">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="71216-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="71216-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71216-144">-Confirm</span></span>
<span data-ttu-id="71216-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71216-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71216-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71216-146">-WhatIf</span></span>
<span data-ttu-id="71216-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71216-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71216-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71216-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71216-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71216-149">CommonParameters</span></span>
<span data-ttu-id="71216-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71216-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71216-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71216-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71216-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71216-152">INPUTS</span></span>

### <span data-ttu-id="71216-153">System. String</span><span class="sxs-lookup"><span data-stu-id="71216-153">System.String</span></span>

### <span data-ttu-id="71216-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71216-154">System.Int32</span></span>

## <span data-ttu-id="71216-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71216-155">OUTPUTS</span></span>

### <span data-ttu-id="71216-156">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="71216-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="71216-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71216-157">NOTES</span></span>

## <span data-ttu-id="71216-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71216-158">RELATED LINKS</span></span>

[<span data-ttu-id="71216-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71216-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="71216-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="71216-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="71216-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="71216-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="71216-162">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="71216-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)