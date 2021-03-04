---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: f410ba5dc89f29c3a928ed459be87769bf5ffca7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886475"
---
# <span data-ttu-id="e7054-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e7054-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="e7054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7054-102">SYNOPSIS</span></span>
<span data-ttu-id="e7054-103">Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="e7054-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e7054-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7054-104">SYNTAX</span></span>

### <span data-ttu-id="e7054-105">DetachExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e7054-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e7054-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e7054-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7054-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7054-107">DESCRIPTION</span></span>
<span data-ttu-id="e7054-108">Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="e7054-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e7054-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7054-109">EXAMPLES</span></span>

### <span data-ttu-id="e7054-110">Exemplo 1: desconectar um banco de dados de seguidores</span><span class="sxs-lookup"><span data-stu-id="e7054-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="e7054-111">O comando acima desconecta o banco de dados de seguidores definido em AttachedDatabaseConfiguration "myfollowerconfiguration" do cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="e7054-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="e7054-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7054-112">PARAMETERS</span></span>

### <span data-ttu-id="e7054-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7054-113">-AsJob</span></span>
<span data-ttu-id="e7054-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e7054-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e7054-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e7054-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="e7054-116">Nome do recurso da configuração de banco de dados anexada no cluster de seguidores.</span><span class="sxs-lookup"><span data-stu-id="e7054-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="e7054-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e7054-117">-ClusterName</span></span>
<span data-ttu-id="e7054-118">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7054-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7054-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="e7054-119">-ClusterResourceId</span></span>
<span data-ttu-id="e7054-120">ID de recurso do cluster que segue um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="e7054-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="e7054-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7054-121">-DefaultProfile</span></span>
<span data-ttu-id="e7054-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7054-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7054-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7054-123">-InputObject</span></span>
<span data-ttu-id="e7054-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e7054-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7054-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e7054-125">-NoWait</span></span>
<span data-ttu-id="e7054-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e7054-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e7054-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7054-127">-PassThru</span></span>
<span data-ttu-id="e7054-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e7054-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e7054-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7054-129">-ResourceGroupName</span></span>
<span data-ttu-id="e7054-130">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7054-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7054-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7054-131">-SubscriptionId</span></span>
<span data-ttu-id="e7054-132">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7054-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7054-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e7054-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7054-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7054-134">-Confirm</span></span>
<span data-ttu-id="e7054-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7054-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7054-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7054-136">-WhatIf</span></span>
<span data-ttu-id="e7054-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7054-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7054-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7054-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7054-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7054-139">CommonParameters</span></span>
<span data-ttu-id="e7054-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7054-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7054-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7054-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7054-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7054-142">INPUTS</span></span>

### <span data-ttu-id="e7054-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e7054-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e7054-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7054-144">OUTPUTS</span></span>

### <span data-ttu-id="e7054-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7054-145">System.Boolean</span></span>

## <span data-ttu-id="e7054-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7054-146">NOTES</span></span>

<span data-ttu-id="e7054-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e7054-147">ALIASES</span></span>

<span data-ttu-id="e7054-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e7054-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7054-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e7054-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7054-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e7054-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7054-151">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e7054-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7054-152">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="e7054-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e7054-153">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7054-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e7054-154">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="e7054-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e7054-155">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7054-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e7054-156">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e7054-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7054-157">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7054-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e7054-158">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e7054-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e7054-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7054-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e7054-160">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7054-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e7054-161">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e7054-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e7054-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7054-162">RELATED LINKS</span></span>

