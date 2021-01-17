---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433581"
---
# <span data-ttu-id="1a73a-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="1a73a-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="1a73a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a73a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a73a-103">Desanexa todos os seguidores de um banco de dados pertencente a este cluster.</span><span class="sxs-lookup"><span data-stu-id="1a73a-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="1a73a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a73a-104">SYNTAX</span></span>

### <span data-ttu-id="1a73a-105">DetachExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a73a-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1a73a-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1a73a-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1a73a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a73a-107">DESCRIPTION</span></span>
<span data-ttu-id="1a73a-108">Desanexa todos os seguidores de um banco de dados pertencente a este cluster.</span><span class="sxs-lookup"><span data-stu-id="1a73a-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="1a73a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a73a-109">EXAMPLES</span></span>

### <span data-ttu-id="1a73a-110">Exemplo 1: desanexar um banco de dados de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="1a73a-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="1a73a-111">O comando acima desanexa o banco de dados de acompanhamento definido em AttachedDatabaseConfiguration "myfollowerconfiguration" do cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="1a73a-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="1a73a-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a73a-112">PARAMETERS</span></span>

### <span data-ttu-id="1a73a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a73a-113">-AsJob</span></span>
<span data-ttu-id="1a73a-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="1a73a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1a73a-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1a73a-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="1a73a-116">Nome do recurso da configuração de banco de dados anexada no cluster de acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="1a73a-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="1a73a-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1a73a-117">-ClusterName</span></span>
<span data-ttu-id="1a73a-118">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1a73a-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="1a73a-119">-ClusterResourceId</span></span>
<span data-ttu-id="1a73a-120">ID do recurso do cluster que segue um banco de dados de propriedade deste cluster.</span><span class="sxs-lookup"><span data-stu-id="1a73a-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="1a73a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a73a-121">-DefaultProfile</span></span>
<span data-ttu-id="1a73a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a73a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a73a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a73a-123">-InputObject</span></span>
<span data-ttu-id="1a73a-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1a73a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1a73a-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1a73a-125">-NoWait</span></span>
<span data-ttu-id="1a73a-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="1a73a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a73a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a73a-127">-PassThru</span></span>
<span data-ttu-id="1a73a-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="1a73a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1a73a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a73a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1a73a-130">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1a73a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a73a-131">-SubscriptionId</span></span>
<span data-ttu-id="1a73a-132">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a73a-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1a73a-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a73a-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1a73a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a73a-134">-Confirm</span></span>
<span data-ttu-id="1a73a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a73a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a73a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a73a-136">-WhatIf</span></span>
<span data-ttu-id="1a73a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a73a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a73a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a73a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a73a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a73a-139">CommonParameters</span></span>
<span data-ttu-id="1a73a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a73a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a73a-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a73a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a73a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a73a-142">INPUTS</span></span>

### <span data-ttu-id="1a73a-143">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1a73a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1a73a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a73a-144">OUTPUTS</span></span>

### <span data-ttu-id="1a73a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a73a-145">System.Boolean</span></span>

## <span data-ttu-id="1a73a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a73a-146">NOTES</span></span>

<span data-ttu-id="1a73a-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1a73a-147">ALIASES</span></span>

<span data-ttu-id="1a73a-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="1a73a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a73a-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1a73a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a73a-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a73a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a73a-151">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="1a73a-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a73a-152">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="1a73a-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1a73a-153">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1a73a-154">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="1a73a-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1a73a-155">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1a73a-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1a73a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a73a-157">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a73a-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1a73a-158">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1a73a-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="1a73a-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1a73a-160">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a73a-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1a73a-161">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a73a-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1a73a-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a73a-162">RELATED LINKS</span></span>

