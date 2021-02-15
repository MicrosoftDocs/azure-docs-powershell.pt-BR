---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118951"
---
# <span data-ttu-id="2cf1f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="2cf1f-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="2cf1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cf1f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf1f-103">Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="2cf1f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cf1f-104">SYNTAX</span></span>

### <span data-ttu-id="2cf1f-105">DetachExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2cf1f-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cf1f-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2cf1f-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2cf1f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cf1f-107">DESCRIPTION</span></span>
<span data-ttu-id="2cf1f-108">Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="2cf1f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2cf1f-109">EXAMPLES</span></span>

### <span data-ttu-id="2cf1f-110">Exemplo 1: Desvincular um banco de dados de seguidores</span><span class="sxs-lookup"><span data-stu-id="2cf1f-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="2cf1f-111">O comando acima desconecta o banco de dados de seguidore definido em AttachedDatabaseConfiguration "myfollowerconfiguration" de cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="2cf1f-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="2cf1f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cf1f-112">PARAMETERS</span></span>

### <span data-ttu-id="2cf1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cf1f-113">-AsJob</span></span>
<span data-ttu-id="2cf1f-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2cf1f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2cf1f-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2cf1f-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="2cf1f-116">Nome do recurso da configuração de banco de dados anexada no cluster de seguidores.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="2cf1f-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2cf1f-117">-ClusterName</span></span>
<span data-ttu-id="2cf1f-118">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2cf1f-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="2cf1f-119">-ClusterResourceId</span></span>
<span data-ttu-id="2cf1f-120">ID do recurso do cluster que segue um banco de dados pertencente a esse cluster.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="2cf1f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf1f-121">-DefaultProfile</span></span>
<span data-ttu-id="2cf1f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf1f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf1f-123">-InputObject</span></span>
<span data-ttu-id="2cf1f-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2cf1f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2cf1f-125">-NoWait</span></span>
<span data-ttu-id="2cf1f-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="2cf1f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2cf1f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cf1f-127">-PassThru</span></span>
<span data-ttu-id="2cf1f-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="2cf1f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2cf1f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf1f-129">-ResourceGroupName</span></span>
<span data-ttu-id="2cf1f-130">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2cf1f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2cf1f-131">-SubscriptionId</span></span>
<span data-ttu-id="2cf1f-132">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2cf1f-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2cf1f-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2cf1f-134">-Confirm</span></span>
<span data-ttu-id="2cf1f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf1f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf1f-136">-WhatIf</span></span>
<span data-ttu-id="2cf1f-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf1f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf1f-139">CommonParameters</span></span>
<span data-ttu-id="2cf1f-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf1f-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cf1f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf1f-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="2cf1f-142">INPUTS</span></span>

### <span data-ttu-id="2cf1f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2cf1f-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2cf1f-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="2cf1f-144">OUTPUTS</span></span>

### <span data-ttu-id="2cf1f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2cf1f-145">System.Boolean</span></span>

## <span data-ttu-id="2cf1f-146">Notas</span><span class="sxs-lookup"><span data-stu-id="2cf1f-146">NOTES</span></span>

<span data-ttu-id="2cf1f-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="2cf1f-147">ALIASES</span></span>

<span data-ttu-id="2cf1f-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="2cf1f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2cf1f-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2cf1f-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2cf1f-151">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="2cf1f-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2cf1f-152">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2cf1f-153">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2cf1f-154">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2cf1f-155">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2cf1f-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="2cf1f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2cf1f-157">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2cf1f-158">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2cf1f-159">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2cf1f-160">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2cf1f-161">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2cf1f-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2cf1f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cf1f-162">RELATED LINKS</span></span>

