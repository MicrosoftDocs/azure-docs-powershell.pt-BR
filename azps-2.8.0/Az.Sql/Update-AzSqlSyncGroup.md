---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: dd8c330e8c81b8e94acc52abc8fe993fc27874ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773982"
---
# <span data-ttu-id="f8b13-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f8b13-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="f8b13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b13-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b13-103">Atualiza um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b13-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f8b13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b13-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8b13-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b13-106">O cmdlet **Update-AzSqlSyncGroup** modifica as propriedades de um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b13-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f8b13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8b13-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b13-108">Exemplo 1: atualizar um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b13-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="f8b13-109">Esse comando atualiza um grupo de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b13-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="f8b13-110">"schema.jsem" é um arquivo no disco local.</span><span class="sxs-lookup"><span data-stu-id="f8b13-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="f8b13-111">Ele contém a carga do esquema no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="f8b13-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="f8b13-112">Um exemplo do esquema JSON é: {"Tables": [{"Columnsname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"Quotname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "Quotname": "MayQuotedTable1"}, {"Columns": [{"quotname": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "quotname": "MayQuotedTable2--MasterSyncMemberName-"}], "quotname": ""}], "": nulo} 7614-4644</span><span class="sxs-lookup"><span data-stu-id="f8b13-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="f8b13-113">OS</span><span class="sxs-lookup"><span data-stu-id="f8b13-113">PARAMETERS</span></span>

### <span data-ttu-id="f8b13-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f8b13-114">-DatabaseCredential</span></span>
<span data-ttu-id="f8b13-115">A credencial de autenticação SQL do banco de dados Hub.</span><span class="sxs-lookup"><span data-stu-id="f8b13-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="f8b13-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8b13-116">-DatabaseName</span></span>
<span data-ttu-id="f8b13-117">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f8b13-117">SQL Database name.</span></span>

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

### <span data-ttu-id="f8b13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b13-118">-DefaultProfile</span></span>
<span data-ttu-id="f8b13-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f8b13-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8b13-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f8b13-120">-IntervalInSeconds</span></span>
<span data-ttu-id="f8b13-121">A frequência (em segundos) de sincronização de dados.</span><span class="sxs-lookup"><span data-stu-id="f8b13-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="f8b13-122">O padrão é-1, o que significa que a sincronização automática não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f8b13-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="f8b13-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b13-123">-Name</span></span>
<span data-ttu-id="f8b13-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f8b13-124">The sync group name.</span></span>

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

### <span data-ttu-id="f8b13-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b13-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8b13-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f8b13-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8b13-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="f8b13-127">-SchemaFile</span></span>
<span data-ttu-id="f8b13-128">O caminho do arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="f8b13-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="f8b13-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f8b13-129">-ServerName</span></span>
<span data-ttu-id="f8b13-130">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f8b13-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f8b13-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8b13-131">-Confirm</span></span>
<span data-ttu-id="f8b13-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8b13-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b13-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b13-133">-WhatIf</span></span>
<span data-ttu-id="f8b13-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8b13-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b13-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8b13-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b13-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b13-136">CommonParameters</span></span>
<span data-ttu-id="f8b13-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b13-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b13-138">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8b13-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b13-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8b13-139">INPUTS</span></span>

### <span data-ttu-id="f8b13-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b13-140">System.String</span></span>

## <span data-ttu-id="f8b13-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8b13-141">OUTPUTS</span></span>

### <span data-ttu-id="f8b13-142">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="f8b13-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f8b13-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8b13-143">NOTES</span></span>

## <span data-ttu-id="f8b13-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b13-144">RELATED LINKS</span></span>

[<span data-ttu-id="f8b13-145">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f8b13-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="f8b13-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f8b13-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="f8b13-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f8b13-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
