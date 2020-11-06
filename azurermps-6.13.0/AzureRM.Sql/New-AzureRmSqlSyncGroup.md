---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 9df59edf3b73597e639e49a13265468b495fe4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431293"
---
# <span data-ttu-id="a221d-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a221d-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="a221d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a221d-102">SYNOPSIS</span></span>
<span data-ttu-id="a221d-103">Cria um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a221d-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a221d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a221d-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a221d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a221d-105">DESCRIPTION</span></span>
<span data-ttu-id="a221d-106">O cmdlet **New-AzureRmSqlSyncGroup** cria um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a221d-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a221d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a221d-107">EXAMPLES</span></span>

### <span data-ttu-id="a221d-108">Exemplo 1: criar um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a221d-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="a221d-109">Esse comando cria um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a221d-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="a221d-110">"schema.jsem" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="a221d-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="a221d-111">Ele contém a carga Shema no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="a221d-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="a221d-112">Um exemplo do esquema JSON é: {"Tables": [{"Columnsname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"Quotname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "Quotname": "MayQuotedTable1"}, {"Columns": [{"quotname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "quotname": "MayQuotedTable2--MasterSyncMemberName-"}], "quotname": ""}], "": nulo} 7614-4644</span><span class="sxs-lookup"><span data-stu-id="a221d-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="a221d-113">OS</span><span class="sxs-lookup"><span data-stu-id="a221d-113">PARAMETERS</span></span>

### <span data-ttu-id="a221d-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a221d-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a221d-115">A política de solução de conflito entre o banco de dados de Hub e membro no grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a221d-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="a221d-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a221d-116">-DatabaseCredential</span></span>
<span data-ttu-id="a221d-117">A credencial de autenticação SQL do banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="a221d-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="a221d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a221d-118">-DatabaseName</span></span>
<span data-ttu-id="a221d-119">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a221d-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a221d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a221d-120">-DefaultProfile</span></span>
<span data-ttu-id="a221d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a221d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a221d-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a221d-122">-IntervalInSeconds</span></span>
<span data-ttu-id="a221d-123">A frequência (em segundos) de sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="a221d-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="a221d-124">O padrão é-1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a221d-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="a221d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a221d-125">-Name</span></span>
<span data-ttu-id="a221d-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a221d-126">The sync group name.</span></span>

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

### <span data-ttu-id="a221d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a221d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a221d-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a221d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a221d-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="a221d-129">-SchemaFile</span></span>
<span data-ttu-id="a221d-130">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="a221d-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="a221d-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a221d-131">-ServerName</span></span>
<span data-ttu-id="a221d-132">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a221d-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a221d-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a221d-133">-SyncDatabaseName</span></span>
<span data-ttu-id="a221d-134">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="a221d-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="a221d-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a221d-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="a221d-136">O grupo de recursos ao qual pertence o banco de dados sincronizar metadados.</span><span class="sxs-lookup"><span data-stu-id="a221d-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="a221d-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="a221d-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="a221d-138">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="a221d-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="a221d-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a221d-139">-Confirm</span></span>
<span data-ttu-id="a221d-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a221d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a221d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a221d-141">-WhatIf</span></span>
<span data-ttu-id="a221d-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a221d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a221d-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a221d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a221d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a221d-144">CommonParameters</span></span>
<span data-ttu-id="a221d-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a221d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a221d-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a221d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a221d-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a221d-147">INPUTS</span></span>

### <span data-ttu-id="a221d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a221d-148">System.String</span></span>

## <span data-ttu-id="a221d-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a221d-149">OUTPUTS</span></span>

### <span data-ttu-id="a221d-150">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a221d-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a221d-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a221d-151">NOTES</span></span>

## <span data-ttu-id="a221d-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a221d-152">RELATED LINKS</span></span>

[<span data-ttu-id="a221d-153">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a221d-153">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a221d-154">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a221d-154">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a221d-155">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a221d-155">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

