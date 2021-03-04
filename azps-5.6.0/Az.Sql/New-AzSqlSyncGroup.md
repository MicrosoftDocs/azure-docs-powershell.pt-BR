---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: fcf973b31312fc525d7a1ae0c2bef84072b0cf9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887659"
---
# <span data-ttu-id="1ba2c-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1ba2c-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="1ba2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba2c-103">Cria um grupo de sincronização SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1ba2c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ba2c-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba2c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ba2c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba2c-106">O cmdlet **New-AzSqlSyncGroup** cria um Grupo de Sincronização de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1ba2c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba2c-108">Exemplo 1: Criar um grupo de sincronização para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="1ba2c-109">Este comando cria um grupo de sincronização para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="1ba2c-110">"schema.json" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="1ba2c-111">Ele contém a carga de esquema no formato json.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="1ba2c-112">Um exemplo do esquema json é: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="1ba2c-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="1ba2c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-113">PARAMETERS</span></span>

### <span data-ttu-id="1ba2c-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ba2c-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="1ba2c-115">A política de resolução de conflitos entre hub e banco de dados de membros no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="1ba2c-116">-DatabaseCredential</span></span>
<span data-ttu-id="1ba2c-117">A SQL de autenticação do banco de dados de hub.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-118">-DatabaseName</span></span>
<span data-ttu-id="1ba2c-119">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1ba2c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba2c-120">-DefaultProfile</span></span>
<span data-ttu-id="1ba2c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1ba2c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ba2c-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1ba2c-122">-IntervalInSeconds</span></span>
<span data-ttu-id="1ba2c-123">A frequência (em segundos) da sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="1ba2c-124">O padrão é -1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1ba2c-125">-Name</span></span>
<span data-ttu-id="1ba2c-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ba2c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ba2c-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="1ba2c-129">-SchemaFile</span></span>
<span data-ttu-id="1ba2c-130">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="1ba2c-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-131">-ServerName</span></span>
<span data-ttu-id="1ba2c-132">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1ba2c-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-133">-SyncDatabaseName</span></span>
<span data-ttu-id="1ba2c-134">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="1ba2c-136">O grupo de recursos ao que o banco de dados de metadados de sincronização pertence.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="1ba2c-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="1ba2c-138">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba2c-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="1ba2c-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="1ba2c-140">Use uma conexão de link privado ao se conectar ao hub deste grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="1ba2c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ba2c-141">-Confirm</span></span>
<span data-ttu-id="1ba2c-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba2c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba2c-143">-WhatIf</span></span>
<span data-ttu-id="1ba2c-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba2c-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba2c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba2c-146">CommonParameters</span></span>
<span data-ttu-id="1ba2c-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba2c-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ba2c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba2c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-149">INPUTS</span></span>

### <span data-ttu-id="1ba2c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba2c-150">System.String</span></span>

## <span data-ttu-id="1ba2c-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-151">OUTPUTS</span></span>

### <span data-ttu-id="1ba2c-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1ba2c-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1ba2c-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ba2c-153">NOTES</span></span>

## <span data-ttu-id="1ba2c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ba2c-154">RELATED LINKS</span></span>

[<span data-ttu-id="1ba2c-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1ba2c-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="1ba2c-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1ba2c-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="1ba2c-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1ba2c-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

