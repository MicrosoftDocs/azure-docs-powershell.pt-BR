---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113703"
---
# <span data-ttu-id="cb4c0-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="cb4c0-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="cb4c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4c0-103">Atualiza um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="cb4c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb4c0-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb4c0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="cb4c0-106">O cmdlet **Update-AzSqlSyncGroup** modifica as propriedades de um Grupo de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="cb4c0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cb4c0-107">EXAMPLES</span></span>

### <span data-ttu-id="cb4c0-108">Exemplo 1: Atualizar um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="cb4c0-109">Esse comando atualiza um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="cb4c0-110">"schema.jsem" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="cb4c0-111">Ele contém a carga de esquema no formato json.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="cb4c0-112">Um exemplo do esquema json é: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Colunas": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="cb4c0-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="cb4c0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb4c0-113">PARAMETERS</span></span>

### <span data-ttu-id="cb4c0-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="cb4c0-114">-DatabaseCredential</span></span>
<span data-ttu-id="cb4c0-115">A credencial de autenticação SQL do banco de dados do hub.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="cb4c0-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="cb4c0-116">-DatabaseName</span></span>
<span data-ttu-id="cb4c0-117">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-117">SQL Database name.</span></span>

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

### <span data-ttu-id="cb4c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4c0-118">-DefaultProfile</span></span>
<span data-ttu-id="cb4c0-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cb4c0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb4c0-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cb4c0-120">-IntervalInSeconds</span></span>
<span data-ttu-id="cb4c0-121">A frequência (em segundos) da sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="cb4c0-122">O padrão é -1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="cb4c0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb4c0-123">-Name</span></span>
<span data-ttu-id="cb4c0-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-124">The sync group name.</span></span>

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

### <span data-ttu-id="cb4c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb4c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb4c0-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb4c0-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="cb4c0-127">-SchemaFile</span></span>
<span data-ttu-id="cb4c0-128">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="cb4c0-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb4c0-129">-ServerName</span></span>
<span data-ttu-id="cb4c0-130">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="cb4c0-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="cb4c0-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="cb4c0-132">Se você quer usar uma conexão de link particular ao se conectar ao hub deste grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="cb4c0-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cb4c0-133">-Confirm</span></span>
<span data-ttu-id="cb4c0-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb4c0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb4c0-135">-WhatIf</span></span>
<span data-ttu-id="cb4c0-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb4c0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb4c0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4c0-138">CommonParameters</span></span>
<span data-ttu-id="cb4c0-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb4c0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4c0-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb4c0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4c0-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="cb4c0-141">INPUTS</span></span>

### <span data-ttu-id="cb4c0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cb4c0-142">System.String</span></span>

## <span data-ttu-id="cb4c0-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="cb4c0-143">OUTPUTS</span></span>

### <span data-ttu-id="cb4c0-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="cb4c0-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="cb4c0-145">Notas</span><span class="sxs-lookup"><span data-stu-id="cb4c0-145">NOTES</span></span>

## <span data-ttu-id="cb4c0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb4c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="cb4c0-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="cb4c0-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="cb4c0-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="cb4c0-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="cb4c0-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="cb4c0-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

