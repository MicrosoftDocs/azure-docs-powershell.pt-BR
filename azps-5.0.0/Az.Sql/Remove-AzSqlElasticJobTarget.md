---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118472"
---
# <span data-ttu-id="f30af-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="f30af-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="f30af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f30af-102">SYNOPSIS</span></span>
<span data-ttu-id="f30af-103">Remove o destino do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="f30af-103">Removes the target from the target group</span></span>

## <span data-ttu-id="f30af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f30af-104">SYNTAX</span></span>

### <span data-ttu-id="f30af-105">SQLDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="f30af-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="f30af-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="f30af-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f30af-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f30af-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f30af-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f30af-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f30af-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30af-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f30af-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f30af-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f30af-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30af-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f30af-114">DESCRIPTION</span></span>
<span data-ttu-id="f30af-115">O cmdlet Remove-AzSqlElasticJobTarget remove um recurso de destino para um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="f30af-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="f30af-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f30af-116">EXAMPLES</span></span>

### <span data-ttu-id="f30af-117">Exemplo 1: remover um destino de servidor</span><span class="sxs-lookup"><span data-stu-id="f30af-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="f30af-118">Exemplo 2: remover um destino de banco de dados</span><span class="sxs-lookup"><span data-stu-id="f30af-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="f30af-119">Exemplo 3: remover um destino de pool elástico</span><span class="sxs-lookup"><span data-stu-id="f30af-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="f30af-120">Exemplo 4: remover um destino do mapa de fragmentos</span><span class="sxs-lookup"><span data-stu-id="f30af-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="f30af-121">Remove um destino (servidor, pool elástico, banco de dados e mapa de fragmentos) de um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="f30af-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="f30af-122">OS</span><span class="sxs-lookup"><span data-stu-id="f30af-122">PARAMETERS</span></span>

### <span data-ttu-id="f30af-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f30af-123">-AgentName</span></span>
<span data-ttu-id="f30af-124">Nome do agente do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f30af-124">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="f30af-125">-AgentServerName</span></span>
<span data-ttu-id="f30af-126">Nome do servidor do SQL Database Agent.</span><span class="sxs-lookup"><span data-stu-id="f30af-126">SQL Database Agent Server Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f30af-127">-DatabaseName</span></span>
<span data-ttu-id="f30af-128">Nome do destino do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f30af-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30af-129">-DefaultProfile</span></span>
<span data-ttu-id="f30af-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f30af-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30af-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f30af-131">-ElasticPoolName</span></span>
<span data-ttu-id="f30af-132">Nome do destino do pool elástico</span><span class="sxs-lookup"><span data-stu-id="f30af-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f30af-133">-ParentObject</span></span>
<span data-ttu-id="f30af-134">Objeto do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="f30af-134">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f30af-135">-ParentResourceId</span></span>
<span data-ttu-id="f30af-136">A ID do recurso do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="f30af-136">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="f30af-137">-RefreshCredentialName</span></span>
<span data-ttu-id="f30af-138">Atualizar nome da credencial</span><span class="sxs-lookup"><span data-stu-id="f30af-138">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30af-139">-ResourceGroupName</span></span>
<span data-ttu-id="f30af-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f30af-140">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-141">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f30af-141">-ServerName</span></span>
<span data-ttu-id="f30af-142">Nome do destino do servidor</span><span class="sxs-lookup"><span data-stu-id="f30af-142">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="f30af-143">-ShardMapName</span></span>
<span data-ttu-id="f30af-144">Nome do destino do mapa de fragmentos</span><span class="sxs-lookup"><span data-stu-id="f30af-144">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f30af-145">-TargetGroupName</span></span>
<span data-ttu-id="f30af-146">Nome do agente do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f30af-146">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f30af-147">-Confirm</span></span>
<span data-ttu-id="f30af-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f30af-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30af-149">-WhatIf</span></span>
<span data-ttu-id="f30af-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f30af-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30af-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f30af-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30af-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30af-152">CommonParameters</span></span>
<span data-ttu-id="f30af-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30af-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30af-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f30af-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30af-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f30af-155">INPUTS</span></span>

### <span data-ttu-id="f30af-156">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f30af-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f30af-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f30af-157">OUTPUTS</span></span>

### <span data-ttu-id="f30af-158">Microsoft. Azure. Management. Sql. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="f30af-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="f30af-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f30af-159">NOTES</span></span>

## <span data-ttu-id="f30af-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f30af-160">RELATED LINKS</span></span>
