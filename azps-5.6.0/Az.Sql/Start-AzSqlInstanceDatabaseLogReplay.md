---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: ce937cc6f7e4bc68592ed089a3028e2919fde29f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886834"
---
# <span data-ttu-id="e1568-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="e1568-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="e1568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1568-102">SYNOPSIS</span></span>
<span data-ttu-id="e1568-103">Inicia um serviço de Repetição de Log com os parâmetros determinados.</span><span class="sxs-lookup"><span data-stu-id="e1568-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="e1568-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1568-104">SYNTAX</span></span>

### <span data-ttu-id="e1568-105">LogReplayInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1568-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1568-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e1568-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-AsJob] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1568-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1568-107">DESCRIPTION</span></span>
<span data-ttu-id="e1568-108">O cmdlet **Start-AzSqlInstanceDatabaseLogReplay** inicia o início do serviço de repetição de log.</span><span class="sxs-lookup"><span data-stu-id="e1568-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="e1568-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1568-109">EXAMPLES</span></span>

### <span data-ttu-id="e1568-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1568-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="e1568-111">Este comando criará um novo banco de dados gerenciado e começará a restaurar backups do contêiner determinado até que last_backup.bak seja restaurado.</span><span class="sxs-lookup"><span data-stu-id="e1568-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="e1568-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e1568-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="e1568-113">Esse comando criará um novo banco de dados gerenciado e começará a restaurar backups do contêiner determinado até que Complete-AzSqlInstanceDatabaseLogReplay seja chamado com o último backup procurado.</span><span class="sxs-lookup"><span data-stu-id="e1568-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="e1568-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1568-114">PARAMETERS</span></span>

### <span data-ttu-id="e1568-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1568-115">-AsJob</span></span>
<span data-ttu-id="e1568-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e1568-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1568-117">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="e1568-117">-AutoCompleteRestore</span></span>
<span data-ttu-id="e1568-118">O indicador se a restauração será concluída automaticamente após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="e1568-118">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="e1568-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="e1568-119">-Collation</span></span>
<span data-ttu-id="e1568-120">O colamento do banco de dados de instância a ser usado.</span><span class="sxs-lookup"><span data-stu-id="e1568-120">The collation of the instance database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1568-121">-DefaultProfile</span></span>
<span data-ttu-id="e1568-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1568-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1568-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1568-123">-InputObject</span></span>
<span data-ttu-id="e1568-124">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="e1568-124">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-125">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e1568-125">-InstanceName</span></span>
<span data-ttu-id="e1568-126">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="e1568-126">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-127">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="e1568-127">-LastBackupName</span></span>
<span data-ttu-id="e1568-128">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="e1568-128">The name of the last backup file to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e1568-129">-Name</span></span>
<span data-ttu-id="e1568-130">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="e1568-130">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1568-131">-PassThru</span></span>
<span data-ttu-id="e1568-132">Define Se retornará o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e1568-132">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="e1568-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1568-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1568-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1568-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-135">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="e1568-135">-StorageContainerSasToken</span></span>
<span data-ttu-id="e1568-136">O token Sas do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e1568-136">The storage container Sas token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasToken

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-137">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="e1568-137">-StorageContainerUri</span></span>
<span data-ttu-id="e1568-138">O URI do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e1568-138">The storage container URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Storage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1568-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1568-139">-Confirm</span></span>
<span data-ttu-id="e1568-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1568-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1568-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1568-141">-WhatIf</span></span>
<span data-ttu-id="e1568-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1568-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1568-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1568-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1568-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1568-144">CommonParameters</span></span>
<span data-ttu-id="e1568-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1568-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1568-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1568-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1568-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1568-147">INPUTS</span></span>

### <span data-ttu-id="e1568-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e1568-148">System.String</span></span>

### <span data-ttu-id="e1568-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1568-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e1568-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1568-150">OUTPUTS</span></span>

### <span data-ttu-id="e1568-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1568-151">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e1568-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1568-152">NOTES</span></span>

## <span data-ttu-id="e1568-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1568-153">RELATED LINKS</span></span>
