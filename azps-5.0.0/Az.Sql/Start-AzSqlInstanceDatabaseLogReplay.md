---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Start-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 61a87f61efaa889af830cc7bdaa44bcf0b7fc698
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115648"
---
# <span data-ttu-id="62108-101">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="62108-101">Start-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="62108-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62108-102">SYNOPSIS</span></span>
<span data-ttu-id="62108-103">Inicia um serviço de reprodução de log com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="62108-103">Starts a Log Replay service with the given parameters.</span></span>

## <span data-ttu-id="62108-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62108-104">SYNTAX</span></span>

### <span data-ttu-id="62108-105">LogReplayInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="62108-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-Name] <String>
 [-InstanceName] <String> [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62108-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="62108-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Start-AzSqlInstanceDatabaseLogReplay -StorageContainerUri <String> -StorageContainerSasToken <String>
 [-AutoCompleteRestore] [-LastBackupName <String>] [-Collation <String>] [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62108-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62108-107">DESCRIPTION</span></span>
<span data-ttu-id="62108-108">O cmdlet **Start-AzSqlInstanceDatabaseLogReplay** inicia o início do serviço de reprodução de log.</span><span class="sxs-lookup"><span data-stu-id="62108-108">The **Start-AzSqlInstanceDatabaseLogReplay** cmdlet initiate start of the log replay service.</span></span>

## <span data-ttu-id="62108-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62108-109">EXAMPLES</span></span>

### <span data-ttu-id="62108-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62108-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
    -AutoComplete -LastBackupName "last_backup.bak"
```

<span data-ttu-id="62108-111">Esse comando criará um novo banco de dados gerenciado e começará a restaurar backups do contêiner especificado até que last_backup. bak seja restaurado.</span><span class="sxs-lookup"><span data-stu-id="62108-111">This command will create new managed database and will start restoring backups from the given container until last_backup.bak is restored.</span></span>

### <span data-ttu-id="62108-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62108-112">Example 2</span></span>
```powershell
PS C:\> Start-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
    -Collation "SQL_Latin1_General_CP1_CI_AS" -StorageContainerUri "https://test.blob.core.windows.net/testing"
    -StorageContainerSasToken "sv=2019-02-02&ss=b&srt=sco&sp=rl&se=2023-12-02T00:09:14Z&st=2019-11-25T16:09:14Z&spr=https&sig=92kAe4QYmXaht%2Fgjocqwerqwer41s%3D"
```

<span data-ttu-id="62108-113">Esse comando criará um novo banco de dados gerenciado e começará a restaurar backups do contêiner fornecido até que o Complete-AzSqlInstanceDatabaseLogReplay seja chamado com o último backup desejado.</span><span class="sxs-lookup"><span data-stu-id="62108-113">This command will create new managed database and will start restoring backups from the given container until Complete-AzSqlInstanceDatabaseLogReplay is called with the last backup wanted.</span></span>

## <span data-ttu-id="62108-114">OS</span><span class="sxs-lookup"><span data-stu-id="62108-114">PARAMETERS</span></span>

### <span data-ttu-id="62108-115">-AutoCompleteRestore</span><span class="sxs-lookup"><span data-stu-id="62108-115">-AutoCompleteRestore</span></span>
<span data-ttu-id="62108-116">O indicador se a restauração automática completa após a conclusão.</span><span class="sxs-lookup"><span data-stu-id="62108-116">The indicator whether or not to auto-complete restore upon completion.</span></span>

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

### <span data-ttu-id="62108-117">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="62108-117">-Collation</span></span>
<span data-ttu-id="62108-118">O agrupamento do banco de dados de instância a ser usado.</span><span class="sxs-lookup"><span data-stu-id="62108-118">The collation of the instance database to use.</span></span>

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

### <span data-ttu-id="62108-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62108-119">-DefaultProfile</span></span>
<span data-ttu-id="62108-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62108-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62108-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62108-121">-InputObject</span></span>
<span data-ttu-id="62108-122">O objeto de banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="62108-122">The instance database object.</span></span>

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

### <span data-ttu-id="62108-123">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="62108-123">-InstanceName</span></span>
<span data-ttu-id="62108-124">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="62108-124">The name of the instance.</span></span>

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

### <span data-ttu-id="62108-125">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="62108-125">-LastBackupName</span></span>
<span data-ttu-id="62108-126">O nome do último arquivo de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="62108-126">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="62108-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="62108-127">-Name</span></span>
<span data-ttu-id="62108-128">O nome do banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="62108-128">The name of the instance database.</span></span>

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

### <span data-ttu-id="62108-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62108-129">-PassThru</span></span>
<span data-ttu-id="62108-130">Define se retorna o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="62108-130">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="62108-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62108-131">-ResourceGroupName</span></span>
<span data-ttu-id="62108-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62108-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="62108-133">-StorageContainerSasToken</span><span class="sxs-lookup"><span data-stu-id="62108-133">-StorageContainerSasToken</span></span>
<span data-ttu-id="62108-134">O token SAS do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62108-134">The storage container Sas token.</span></span>

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

### <span data-ttu-id="62108-135">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="62108-135">-StorageContainerUri</span></span>
<span data-ttu-id="62108-136">O URI do contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62108-136">The storage container URI.</span></span>

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

### <span data-ttu-id="62108-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62108-137">-Confirm</span></span>
<span data-ttu-id="62108-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62108-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62108-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62108-139">-WhatIf</span></span>
<span data-ttu-id="62108-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62108-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62108-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62108-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62108-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62108-142">CommonParameters</span></span>
<span data-ttu-id="62108-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62108-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62108-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62108-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62108-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62108-145">INPUTS</span></span>

### <span data-ttu-id="62108-146">System. String</span><span class="sxs-lookup"><span data-stu-id="62108-146">System.String</span></span>

### <span data-ttu-id="62108-147">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="62108-147">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="62108-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62108-148">OUTPUTS</span></span>

### <span data-ttu-id="62108-149">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="62108-149">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="62108-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62108-150">NOTES</span></span>

## <span data-ttu-id="62108-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62108-151">RELATED LINKS</span></span>
