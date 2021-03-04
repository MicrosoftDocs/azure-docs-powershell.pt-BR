---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: c95b6a7a42327b7380e19ff333453f956797dcdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892696"
---
# <span data-ttu-id="fa731-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa731-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fa731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa731-102">SYNOPSIS</span></span>
<span data-ttu-id="fa731-103">Atualiza um grupo de sincronização SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa731-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fa731-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa731-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa731-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa731-105">DESCRIPTION</span></span>
<span data-ttu-id="fa731-106">O cmdlet **Update-AzSqlSyncGroup** modifica propriedades de um Grupo de Sincronização de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fa731-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fa731-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa731-107">EXAMPLES</span></span>

### <span data-ttu-id="fa731-108">Exemplo 1: atualizar um grupo de sincronização para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fa731-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="fa731-109">Este comando atualiza um grupo de sincronização para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fa731-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="fa731-110">"schema.json" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="fa731-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="fa731-111">Ele contém a carga de esquema no formato json.</span><span class="sxs-lookup"><span data-stu-id="fa731-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="fa731-112">Um exemplo do esquema json é: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="fa731-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="fa731-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa731-113">PARAMETERS</span></span>

### <span data-ttu-id="fa731-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="fa731-114">-DatabaseCredential</span></span>
<span data-ttu-id="fa731-115">A SQL de autenticação do banco de dados de hub.</span><span class="sxs-lookup"><span data-stu-id="fa731-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="fa731-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa731-116">-DatabaseName</span></span>
<span data-ttu-id="fa731-117">SQL Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa731-117">SQL Database name.</span></span>

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

### <span data-ttu-id="fa731-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa731-118">-DefaultProfile</span></span>
<span data-ttu-id="fa731-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fa731-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa731-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fa731-120">-IntervalInSeconds</span></span>
<span data-ttu-id="fa731-121">A frequência (em segundos) da sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="fa731-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="fa731-122">O padrão é -1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fa731-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="fa731-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fa731-123">-Name</span></span>
<span data-ttu-id="fa731-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="fa731-124">The sync group name.</span></span>

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

### <span data-ttu-id="fa731-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa731-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa731-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa731-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa731-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="fa731-127">-SchemaFile</span></span>
<span data-ttu-id="fa731-128">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="fa731-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="fa731-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa731-129">-ServerName</span></span>
<span data-ttu-id="fa731-130">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fa731-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fa731-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fa731-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="fa731-132">Se deve usar uma conexão de link privado ao se conectar ao hub deste grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="fa731-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa731-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa731-133">-Confirm</span></span>
<span data-ttu-id="fa731-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa731-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa731-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa731-135">-WhatIf</span></span>
<span data-ttu-id="fa731-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa731-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa731-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa731-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa731-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa731-138">CommonParameters</span></span>
<span data-ttu-id="fa731-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa731-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa731-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa731-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa731-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa731-141">INPUTS</span></span>

### <span data-ttu-id="fa731-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fa731-142">System.String</span></span>

## <span data-ttu-id="fa731-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa731-143">OUTPUTS</span></span>

### <span data-ttu-id="fa731-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="fa731-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fa731-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa731-145">NOTES</span></span>

## <span data-ttu-id="fa731-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa731-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa731-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa731-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fa731-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa731-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="fa731-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa731-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

