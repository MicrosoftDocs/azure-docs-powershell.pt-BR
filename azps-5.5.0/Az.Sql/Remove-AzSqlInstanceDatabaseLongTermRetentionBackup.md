---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113723"
---
# <span data-ttu-id="492b2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="492b2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="492b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="492b2-102">SYNOPSIS</span></span>
<span data-ttu-id="492b2-103">Exclui um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="492b2-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="492b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="492b2-104">SYNTAX</span></span>

### <span data-ttu-id="492b2-105">RemoveBackupDefault (Padrão)</span><span class="sxs-lookup"><span data-stu-id="492b2-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="492b2-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="492b2-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="492b2-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="492b2-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="492b2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="492b2-108">DESCRIPTION</span></span>
<span data-ttu-id="492b2-109">O cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** exclui o backup especificado.</span><span class="sxs-lookup"><span data-stu-id="492b2-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="492b2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="492b2-110">EXAMPLES</span></span>

### <span data-ttu-id="492b2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="492b2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="492b2-112">Exclui o backup com o nome 15be823c-7e2c-49d8-819f-a3fdcad92215;1322682505500000000</span><span class="sxs-lookup"><span data-stu-id="492b2-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="492b2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="492b2-113">PARAMETERS</span></span>

### <span data-ttu-id="492b2-114">-Nome do Backup</span><span class="sxs-lookup"><span data-stu-id="492b2-114">-BackupName</span></span>
<span data-ttu-id="492b2-115">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="492b2-115">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="492b2-116">-DatabaseName</span></span>
<span data-ttu-id="492b2-117">O nome do Banco de Dados Gerenciado do backup é de.</span><span class="sxs-lookup"><span data-stu-id="492b2-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492b2-118">-DefaultProfile</span></span>
<span data-ttu-id="492b2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="492b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="492b2-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="492b2-120">-Force</span></span>
<span data-ttu-id="492b2-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="492b2-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="492b2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="492b2-122">-InputObject</span></span>
<span data-ttu-id="492b2-123">O objeto Backup de Retenção de Longo Prazo do Banco de Dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="492b2-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-124">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="492b2-124">-InstanceName</span></span>
<span data-ttu-id="492b2-125">O nome da Instância Gerenciada em que o backup está.</span><span class="sxs-lookup"><span data-stu-id="492b2-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-126">-Local</span><span class="sxs-lookup"><span data-stu-id="492b2-126">-Location</span></span>
<span data-ttu-id="492b2-127">O local da Instância Gerenciada de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="492b2-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492b2-128">-ResourceGroupName</span></span>
<span data-ttu-id="492b2-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="492b2-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="492b2-130">-ResourceId</span></span>
<span data-ttu-id="492b2-131">A ID do Recurso do Backup de Retenção de Longo Prazo do Banco de Dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="492b2-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="492b2-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="492b2-132">-Confirm</span></span>
<span data-ttu-id="492b2-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="492b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="492b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="492b2-134">-WhatIf</span></span>
<span data-ttu-id="492b2-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="492b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="492b2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="492b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="492b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492b2-137">CommonParameters</span></span>
<span data-ttu-id="492b2-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492b2-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="492b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492b2-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="492b2-140">INPUTS</span></span>

### <span data-ttu-id="492b2-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="492b2-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="492b2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="492b2-142">System.String</span></span>

## <span data-ttu-id="492b2-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="492b2-143">OUTPUTS</span></span>

### <span data-ttu-id="492b2-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="492b2-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="492b2-145">Notas</span><span class="sxs-lookup"><span data-stu-id="492b2-145">NOTES</span></span>

## <span data-ttu-id="492b2-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="492b2-146">RELATED LINKS</span></span>

[<span data-ttu-id="492b2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="492b2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="492b2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="492b2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="492b2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="492b2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="492b2-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="492b2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)