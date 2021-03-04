---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6fe6e142184059d554922579e669db5815a18c94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885783"
---
# <span data-ttu-id="c8d8c-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="c8d8c-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="c8d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d8c-103">Remove o destino do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="c8d8c-103">Removes the target from the target group</span></span>

## <span data-ttu-id="c8d8c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8d8c-104">SYNTAX</span></span>

### <span data-ttu-id="c8d8c-105">SqlDatabase (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8d8c-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="c8d8c-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="c8d8c-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c8d8c-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c8d8c-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c8d8c-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8c-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8c-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d8c-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8c-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d8c-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8d8c-114">DESCRIPTION</span></span>
<span data-ttu-id="c8d8c-115">O Remove-AzSqlElasticJobTarget cmdlet remove um recurso de destino para um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="c8d8c-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="c8d8c-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-116">EXAMPLES</span></span>

### <span data-ttu-id="c8d8c-117">Exemplo 1: Remover um destino de servidor</span><span class="sxs-lookup"><span data-stu-id="c8d8c-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="c8d8c-118">Exemplo 2: Remover um destino de banco de dados</span><span class="sxs-lookup"><span data-stu-id="c8d8c-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="c8d8c-119">Exemplo 3: Remover um destino de pool elástica</span><span class="sxs-lookup"><span data-stu-id="c8d8c-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="c8d8c-120">Exemplo 4: Remover um destino de mapa de fragmento</span><span class="sxs-lookup"><span data-stu-id="c8d8c-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="c8d8c-121">Remove um destino (servidor, pool elástica, banco de dados e mapa de fragmento) de um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="c8d8c-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="c8d8c-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-122">PARAMETERS</span></span>

### <span data-ttu-id="c8d8c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-123">-AgentName</span></span>
<span data-ttu-id="c8d8c-124">SQL Nome do Agente de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="c8d8c-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-125">-AgentServerName</span></span>
<span data-ttu-id="c8d8c-126">SQL Nome do Servidor do Agente de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="c8d8c-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-127">-DatabaseName</span></span>
<span data-ttu-id="c8d8c-128">Nome de destino do banco de dados</span><span class="sxs-lookup"><span data-stu-id="c8d8c-128">Database Target Name</span></span>

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

### <span data-ttu-id="c8d8c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d8c-129">-DefaultProfile</span></span>
<span data-ttu-id="c8d8c-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d8c-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-131">-ElasticPoolName</span></span>
<span data-ttu-id="c8d8c-132">Nome de destino do pool elástica</span><span class="sxs-lookup"><span data-stu-id="c8d8c-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="c8d8c-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c8d8c-133">-ParentObject</span></span>
<span data-ttu-id="c8d8c-134">O objeto de grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-134">The target group object.</span></span>

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

### <span data-ttu-id="c8d8c-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8c-135">-ParentResourceId</span></span>
<span data-ttu-id="c8d8c-136">A ID de recurso do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-136">The target group resource id.</span></span>

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

### <span data-ttu-id="c8d8c-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-137">-RefreshCredentialName</span></span>
<span data-ttu-id="c8d8c-138">Atualizar Nome da Credencial</span><span class="sxs-lookup"><span data-stu-id="c8d8c-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="c8d8c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-139">-ResourceGroupName</span></span>
<span data-ttu-id="c8d8c-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c8d8c-140">Resource Group Name</span></span>

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

### <span data-ttu-id="c8d8c-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-141">-ServerName</span></span>
<span data-ttu-id="c8d8c-142">Nome do destino do servidor</span><span class="sxs-lookup"><span data-stu-id="c8d8c-142">Server Target Name</span></span>

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

### <span data-ttu-id="c8d8c-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-143">-ShardMapName</span></span>
<span data-ttu-id="c8d8c-144">Nome de destino do mapa de fragmento</span><span class="sxs-lookup"><span data-stu-id="c8d8c-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="c8d8c-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d8c-145">-TargetGroupName</span></span>
<span data-ttu-id="c8d8c-146">SQL Nome do Agente de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="c8d8c-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8d8c-147">-Confirm</span></span>
<span data-ttu-id="c8d8c-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d8c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d8c-149">-WhatIf</span></span>
<span data-ttu-id="c8d8c-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d8c-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d8c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d8c-152">CommonParameters</span></span>
<span data-ttu-id="c8d8c-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d8c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d8c-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8d8c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d8c-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-155">INPUTS</span></span>

### <span data-ttu-id="c8d8c-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="c8d8c-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="c8d8c-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-157">OUTPUTS</span></span>

### <span data-ttu-id="c8d8c-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="c8d8c-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="c8d8c-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8d8c-159">NOTES</span></span>

## <span data-ttu-id="c8d8c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8d8c-160">RELATED LINKS</span></span>
