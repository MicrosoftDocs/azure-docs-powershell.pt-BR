---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 7789bdc098ab7bb02414ffc39f38ba25f1c7e5ae
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399559"
---
# <span data-ttu-id="e27d8-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e27d8-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="e27d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e27d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d8-103">Cria um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e27d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e27d8-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e27d8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e27d8-105">DESCRIPTION</span></span>
<span data-ttu-id="e27d8-106">O cmdlet **New-AzSqlSyncGroup** cria um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e27d8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e27d8-107">EXAMPLES</span></span>

### <span data-ttu-id="e27d8-108">Exemplo 1: Criar um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="e27d8-109">Esse comando cria um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="e27d8-110">"schema.jsem" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="e27d8-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="e27d8-111">Ela contém a carga de shema no formato json.</span><span class="sxs-lookup"><span data-stu-id="e27d8-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="e27d8-112">Um exemplo do esquema json é: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Colunas": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="e27d8-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="e27d8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e27d8-113">PARAMETERS</span></span>

### <span data-ttu-id="e27d8-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d8-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e27d8-115">A política de resolução de conflitos entre o hub e o banco de dados de membros no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e27d8-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="e27d8-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e27d8-116">-DatabaseCredential</span></span>
<span data-ttu-id="e27d8-117">A credencial de autenticação SQL do banco de dados do hub.</span><span class="sxs-lookup"><span data-stu-id="e27d8-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="e27d8-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="e27d8-118">-DatabaseName</span></span>
<span data-ttu-id="e27d8-119">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e27d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d8-120">-DefaultProfile</span></span>
<span data-ttu-id="e27d8-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e27d8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e27d8-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e27d8-122">-IntervalInSeconds</span></span>
<span data-ttu-id="e27d8-123">A frequência (em segundos) da sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="e27d8-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="e27d8-124">O padrão é -1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e27d8-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="e27d8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e27d8-125">-Name</span></span>
<span data-ttu-id="e27d8-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e27d8-126">The sync group name.</span></span>

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

### <span data-ttu-id="e27d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="e27d8-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e27d8-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e27d8-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="e27d8-129">-SchemaFile</span></span>
<span data-ttu-id="e27d8-130">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="e27d8-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="e27d8-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e27d8-131">-ServerName</span></span>
<span data-ttu-id="e27d8-132">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d8-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e27d8-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e27d8-133">-SyncDatabaseName</span></span>
<span data-ttu-id="e27d8-134">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="e27d8-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="e27d8-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d8-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="e27d8-136">O grupo de recursos ao que o banco de dados de metadados de sincronização pertence.</span><span class="sxs-lookup"><span data-stu-id="e27d8-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="e27d8-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="e27d8-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="e27d8-138">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="e27d8-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="e27d8-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e27d8-139">-Confirm</span></span>
<span data-ttu-id="e27d8-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e27d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e27d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e27d8-141">-WhatIf</span></span>
<span data-ttu-id="e27d8-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e27d8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e27d8-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e27d8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e27d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d8-144">CommonParameters</span></span>
<span data-ttu-id="e27d8-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d8-146">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e27d8-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d8-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="e27d8-147">INPUTS</span></span>

### <span data-ttu-id="e27d8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e27d8-148">System.String</span></span>

## <span data-ttu-id="e27d8-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="e27d8-149">OUTPUTS</span></span>

### <span data-ttu-id="e27d8-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e27d8-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e27d8-151">Notas</span><span class="sxs-lookup"><span data-stu-id="e27d8-151">NOTES</span></span>

## <span data-ttu-id="e27d8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e27d8-152">RELATED LINKS</span></span>


[<span data-ttu-id="e27d8-153">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e27d8-153">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="e27d8-154">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e27d8-154">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

