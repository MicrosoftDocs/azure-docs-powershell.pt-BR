---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 3a5c9284da784324b6b0887b836189c58077faa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886577"
---
# <span data-ttu-id="4473c-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="4473c-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="4473c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4473c-102">SYNOPSIS</span></span>
<span data-ttu-id="4473c-103">Adiciona um destino a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="4473c-103">Adds a target to a target group</span></span>

## <span data-ttu-id="4473c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4473c-104">SYNTAX</span></span>

### <span data-ttu-id="4473c-105">SqlDatabase (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4473c-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="4473c-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4473c-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="4473c-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4473c-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4473c-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4473c-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4473c-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4473c-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4473c-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4473c-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4473c-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4473c-114">DESCRIPTION</span></span>
<span data-ttu-id="4473c-115">O Add-AzSqlElasticJobTarget cmdlet adiciona um recurso de destino a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="4473c-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="4473c-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4473c-116">EXAMPLES</span></span>

### <span data-ttu-id="4473c-117">Exemplo 1: Adicionar um destino de servidor</span><span class="sxs-lookup"><span data-stu-id="4473c-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="4473c-118">Exemplo 2: Adicionar um destino de banco de dados</span><span class="sxs-lookup"><span data-stu-id="4473c-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="4473c-119">Exemplo 3: Adicionar um destino de pool elástica</span><span class="sxs-lookup"><span data-stu-id="4473c-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="4473c-120">Exemplo 4: Adicionar um destino de mapa estilhaço</span><span class="sxs-lookup"><span data-stu-id="4473c-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="4473c-121">Adiciona um destino (servidor, pool elástica, banco de dados e mapa de fragmento) a um grupo de destino</span><span class="sxs-lookup"><span data-stu-id="4473c-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="4473c-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4473c-122">PARAMETERS</span></span>

### <span data-ttu-id="4473c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4473c-123">-AgentName</span></span>
<span data-ttu-id="4473c-124">O nome do agente.</span><span class="sxs-lookup"><span data-stu-id="4473c-124">The agent name.</span></span>

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

### <span data-ttu-id="4473c-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="4473c-125">-AgentServerName</span></span>
<span data-ttu-id="4473c-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4473c-126">The server name.</span></span>

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

### <span data-ttu-id="4473c-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4473c-127">-DatabaseName</span></span>
<span data-ttu-id="4473c-128">Nome de destino do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4473c-128">Database Target Name</span></span>

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

### <span data-ttu-id="4473c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4473c-129">-DefaultProfile</span></span>
<span data-ttu-id="4473c-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4473c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4473c-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4473c-131">-ElasticPoolName</span></span>
<span data-ttu-id="4473c-132">Nome de destino do pool elástica</span><span class="sxs-lookup"><span data-stu-id="4473c-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="4473c-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="4473c-133">-Exclude</span></span>
<span data-ttu-id="4473c-134">Exclui um destino.</span><span class="sxs-lookup"><span data-stu-id="4473c-134">Excludes a target.</span></span>

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

### <span data-ttu-id="4473c-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4473c-135">-ParentObject</span></span>
<span data-ttu-id="4473c-136">O objeto de grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="4473c-136">The target group object.</span></span>

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

### <span data-ttu-id="4473c-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4473c-137">-ParentResourceId</span></span>
<span data-ttu-id="4473c-138">A ID de recurso do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="4473c-138">The target group resource id.</span></span>

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

### <span data-ttu-id="4473c-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="4473c-139">-RefreshCredentialName</span></span>
<span data-ttu-id="4473c-140">Atualizar Nome da Credencial</span><span class="sxs-lookup"><span data-stu-id="4473c-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="4473c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4473c-141">-ResourceGroupName</span></span>
<span data-ttu-id="4473c-142">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4473c-142">Resource Group Name</span></span>

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

### <span data-ttu-id="4473c-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4473c-143">-ServerName</span></span>
<span data-ttu-id="4473c-144">Nome do destino do servidor</span><span class="sxs-lookup"><span data-stu-id="4473c-144">Server Target Name</span></span>

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

### <span data-ttu-id="4473c-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="4473c-145">-ShardMapName</span></span>
<span data-ttu-id="4473c-146">Nome de destino do mapa de fragmento</span><span class="sxs-lookup"><span data-stu-id="4473c-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="4473c-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="4473c-147">-TargetGroupName</span></span>
<span data-ttu-id="4473c-148">O nome do grupo de destino.</span><span class="sxs-lookup"><span data-stu-id="4473c-148">The target group name.</span></span>

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

### <span data-ttu-id="4473c-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4473c-149">-Confirm</span></span>
<span data-ttu-id="4473c-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4473c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4473c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4473c-151">-WhatIf</span></span>
<span data-ttu-id="4473c-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4473c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4473c-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4473c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4473c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4473c-154">CommonParameters</span></span>
<span data-ttu-id="4473c-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4473c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4473c-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4473c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4473c-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4473c-157">INPUTS</span></span>

### <span data-ttu-id="4473c-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="4473c-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="4473c-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4473c-159">OUTPUTS</span></span>

### <span data-ttu-id="4473c-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="4473c-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="4473c-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="4473c-161">NOTES</span></span>

## <span data-ttu-id="4473c-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4473c-162">RELATED LINKS</span></span>
