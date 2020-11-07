---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778018"
---
# <span data-ttu-id="7ebac-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ebac-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="7ebac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ebac-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebac-103">O cmdlet **set-AzSqlInstanceDatabaseLongTermRetentionBackup** define a política de retenção de longo prazo do banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7ebac-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="7ebac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ebac-104">SYNTAX</span></span>

### <span data-ttu-id="7ebac-105">WeeklyRetentionRequired (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ebac-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebac-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7ebac-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebac-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7ebac-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebac-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="7ebac-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ebac-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ebac-109">DESCRIPTION</span></span>
<span data-ttu-id="7ebac-110">O cmdlet **set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** define a política de retenção de longa duração para esse banco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7ebac-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="7ebac-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ebac-111">EXAMPLES</span></span>

### <span data-ttu-id="7ebac-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ebac-112">Example 1</span></span>
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

<span data-ttu-id="7ebac-113">Configura a política semanal de retenção de longo prazo do banco de dados para uma semana.</span><span class="sxs-lookup"><span data-stu-id="7ebac-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="7ebac-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7ebac-114">Example 2</span></span>
```
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


<span data-ttu-id="7ebac-115">Esse comando Remove a política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7ebac-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="7ebac-116">OS</span><span class="sxs-lookup"><span data-stu-id="7ebac-116">PARAMETERS</span></span>

### <span data-ttu-id="7ebac-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7ebac-117">-DatabaseName</span></span>
<span data-ttu-id="7ebac-118">O nome do banco de dados gerenciado do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="7ebac-118">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="7ebac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebac-119">-DefaultProfile</span></span>
<span data-ttu-id="7ebac-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7ebac-121">-InstanceName</span></span>
<span data-ttu-id="7ebac-122">O nome da instância gerenciada do Azure à qual o banco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="7ebac-122">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="7ebac-123">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="7ebac-123">-MonthlyRetention</span></span>
<span data-ttu-id="7ebac-124">A retenção mensal.</span><span class="sxs-lookup"><span data-stu-id="7ebac-124">The Monthly Retention.</span></span>
<span data-ttu-id="7ebac-125">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7ebac-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7ebac-126">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7ebac-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="7ebac-127">-RemovePolicy</span></span>
<span data-ttu-id="7ebac-128">Se fornecido, a política para o banco de dados será limpa.</span><span class="sxs-lookup"><span data-stu-id="7ebac-128">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="7ebac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebac-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ebac-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ebac-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ebac-131">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="7ebac-131">-WeeklyRetention</span></span>
<span data-ttu-id="7ebac-132">A retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="7ebac-132">The Weekly Retention.</span></span>
<span data-ttu-id="7ebac-133">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7ebac-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7ebac-134">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7ebac-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="7ebac-135">-WeekOfYear</span></span>
<span data-ttu-id="7ebac-136">A semana do ano, de 1 a 52, para economizar pela retenção anual.</span><span class="sxs-lookup"><span data-stu-id="7ebac-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-137">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="7ebac-137">-YearlyRetention</span></span>
<span data-ttu-id="7ebac-138">A retenção anual.</span><span class="sxs-lookup"><span data-stu-id="7ebac-138">The Yearly Retention.</span></span>
<span data-ttu-id="7ebac-139">Se for passado apenas um número em vez de uma cadeia de caracteres ISO 8601, os dias serão considerados como as unidades.</span><span class="sxs-lookup"><span data-stu-id="7ebac-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="7ebac-140">Há um mínimo de 7 dias e um máximo de 10 anos.</span><span class="sxs-lookup"><span data-stu-id="7ebac-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ebac-141">-Confirm</span></span>
<span data-ttu-id="7ebac-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ebac-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebac-143">-WhatIf</span></span>
<span data-ttu-id="7ebac-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ebac-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebac-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ebac-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebac-146">CommonParameters</span></span>
<span data-ttu-id="7ebac-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebac-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ebac-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebac-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ebac-149">INPUTS</span></span>

### <span data-ttu-id="7ebac-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7ebac-150">System.String</span></span>

### <span data-ttu-id="7ebac-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7ebac-151">System.Int32</span></span>

## <span data-ttu-id="7ebac-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ebac-152">OUTPUTS</span></span>

### <span data-ttu-id="7ebac-153">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7ebac-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="7ebac-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ebac-154">NOTES</span></span>

## <span data-ttu-id="7ebac-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ebac-155">RELATED LINKS</span></span>

[<span data-ttu-id="7ebac-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ebac-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7ebac-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7ebac-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7ebac-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7ebac-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7ebac-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7ebac-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)