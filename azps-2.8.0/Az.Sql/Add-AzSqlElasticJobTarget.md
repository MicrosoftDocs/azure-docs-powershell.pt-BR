---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: d1788abc6ac0546732fe2476cf2822210a1fa8da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772399"
---
# <span data-ttu-id="d1f81-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="d1f81-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="d1f81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1f81-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f81-103">Adiciona um destino a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="d1f81-103">Adds a target to a target group</span></span>

## <span data-ttu-id="d1f81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1f81-104">SYNTAX</span></span>

### <span data-ttu-id="d1f81-105">SQLDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1f81-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="d1f81-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f81-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="d1f81-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d1f81-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d1f81-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d1f81-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f81-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f81-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f81-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f81-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f81-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1f81-114">DESCRIPTION</span></span>
<span data-ttu-id="d1f81-115">O cmdlet Add-AzSqlElasticJobTarget adiciona um recurso de destino a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="d1f81-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="d1f81-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1f81-116">EXAMPLES</span></span>

### <span data-ttu-id="d1f81-117">Exemplo 1-adicionar um destino de servidor</span><span class="sxs-lookup"><span data-stu-id="d1f81-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="d1f81-118">Exemplo 2-adicionar um destino de banco de dados</span><span class="sxs-lookup"><span data-stu-id="d1f81-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="d1f81-119">Exemplo 3-adicionar um destino de pool elástico</span><span class="sxs-lookup"><span data-stu-id="d1f81-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="d1f81-120">Exemplo 4-adicionar um destino do mapa de fragmentos</span><span class="sxs-lookup"><span data-stu-id="d1f81-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="d1f81-121">Adiciona um destino (servidor, pool elástico, banco de dados e mapa de fragmentos) a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="d1f81-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="d1f81-122">OS</span><span class="sxs-lookup"><span data-stu-id="d1f81-122">PARAMETERS</span></span>

### <span data-ttu-id="d1f81-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d1f81-123">-AgentName</span></span>
<span data-ttu-id="d1f81-124">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="d1f81-124">The agent name.</span></span>

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

### <span data-ttu-id="d1f81-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="d1f81-125">-AgentServerName</span></span>
<span data-ttu-id="d1f81-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d1f81-126">The server name.</span></span>

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

### <span data-ttu-id="d1f81-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1f81-127">-DatabaseName</span></span>
<span data-ttu-id="d1f81-128">Nome do destino do banco de dados</span><span class="sxs-lookup"><span data-stu-id="d1f81-128">Database Target Name</span></span>

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

### <span data-ttu-id="d1f81-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f81-129">-DefaultProfile</span></span>
<span data-ttu-id="d1f81-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f81-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f81-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d1f81-131">-ElasticPoolName</span></span>
<span data-ttu-id="d1f81-132">Nome do destino do pool elástico</span><span class="sxs-lookup"><span data-stu-id="d1f81-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="d1f81-133">-Excluir</span><span class="sxs-lookup"><span data-stu-id="d1f81-133">-Exclude</span></span>
<span data-ttu-id="d1f81-134">Exclui um destino.</span><span class="sxs-lookup"><span data-stu-id="d1f81-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f81-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1f81-135">-ParentObject</span></span>
<span data-ttu-id="d1f81-136">Objeto do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="d1f81-136">The target group object.</span></span>

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

### <span data-ttu-id="d1f81-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f81-137">-ParentResourceId</span></span>
<span data-ttu-id="d1f81-138">A ID do recurso do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="d1f81-138">The target group resource id.</span></span>

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

### <span data-ttu-id="d1f81-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="d1f81-139">-RefreshCredentialName</span></span>
<span data-ttu-id="d1f81-140">Atualizar nome da credencial</span><span class="sxs-lookup"><span data-stu-id="d1f81-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="d1f81-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f81-141">-ResourceGroupName</span></span>
<span data-ttu-id="d1f81-142">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d1f81-142">Resource Group Name</span></span>

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

### <span data-ttu-id="d1f81-143">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d1f81-143">-ServerName</span></span>
<span data-ttu-id="d1f81-144">Nome do destino do servidor</span><span class="sxs-lookup"><span data-stu-id="d1f81-144">Server Target Name</span></span>

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

### <span data-ttu-id="d1f81-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="d1f81-145">-ShardMapName</span></span>
<span data-ttu-id="d1f81-146">Nome do destino do mapa de fragmentos</span><span class="sxs-lookup"><span data-stu-id="d1f81-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="d1f81-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f81-147">-TargetGroupName</span></span>
<span data-ttu-id="d1f81-148">O nome do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="d1f81-148">The target group name.</span></span>

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

### <span data-ttu-id="d1f81-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1f81-149">-Confirm</span></span>
<span data-ttu-id="d1f81-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1f81-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f81-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f81-151">-WhatIf</span></span>
<span data-ttu-id="d1f81-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1f81-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f81-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1f81-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f81-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f81-154">CommonParameters</span></span>
<span data-ttu-id="d1f81-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f81-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f81-156">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1f81-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f81-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1f81-157">INPUTS</span></span>

### <span data-ttu-id="d1f81-158">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="d1f81-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="d1f81-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1f81-159">OUTPUTS</span></span>

### <span data-ttu-id="d1f81-160">Microsoft. Azure. Management. Sql. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="d1f81-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="d1f81-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1f81-161">NOTES</span></span>

## <span data-ttu-id="d1f81-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1f81-162">RELATED LINKS</span></span>