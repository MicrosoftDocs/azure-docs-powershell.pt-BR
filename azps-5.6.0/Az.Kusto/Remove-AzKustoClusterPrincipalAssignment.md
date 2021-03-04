---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b2dd7c125fbf2529e7dc214efdc9ef5fdef1ace0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891809"
---
# <span data-ttu-id="bc4d0-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="bc4d0-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="bc4d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4d0-103">Exclui uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="bc4d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc4d0-104">SYNTAX</span></span>

### <span data-ttu-id="bc4d0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc4d0-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc4d0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc4d0-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc4d0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc4d0-107">DESCRIPTION</span></span>
<span data-ttu-id="bc4d0-108">Exclui uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="bc4d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-109">EXAMPLES</span></span>

### <span data-ttu-id="bc4d0-110">Exemplo 1: Excluir um cluster Kusto existente PrincipalAssignment pelo nome</span><span class="sxs-lookup"><span data-stu-id="bc4d0-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="bc4d0-111">O comando acima exclui o PrincipalAssignment chamado "kustoprincipal1" no cluster kusto "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="bc4d0-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="bc4d0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-112">PARAMETERS</span></span>

### <span data-ttu-id="bc4d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc4d0-113">-AsJob</span></span>
<span data-ttu-id="bc4d0-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bc4d0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="bc4d0-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bc4d0-115">-ClusterName</span></span>
<span data-ttu-id="bc4d0-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4d0-117">-DefaultProfile</span></span>
<span data-ttu-id="bc4d0-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc4d0-119">-InputObject</span></span>
<span data-ttu-id="bc4d0-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4d0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bc4d0-121">-NoWait</span></span>
<span data-ttu-id="bc4d0-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="bc4d0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc4d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc4d0-123">-PassThru</span></span>
<span data-ttu-id="bc4d0-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bc4d0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bc4d0-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="bc4d0-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="bc4d0-126">O nome da entidade KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-126">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc4d0-128">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4d0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc4d0-129">-SubscriptionId</span></span>
<span data-ttu-id="bc4d0-130">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc4d0-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4d0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc4d0-132">-Confirm</span></span>
<span data-ttu-id="bc4d0-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4d0-134">-WhatIf</span></span>
<span data-ttu-id="bc4d0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc4d0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4d0-137">CommonParameters</span></span>
<span data-ttu-id="bc4d0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4d0-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc4d0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4d0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-140">INPUTS</span></span>

### <span data-ttu-id="bc4d0-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="bc4d0-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="bc4d0-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-142">OUTPUTS</span></span>

### <span data-ttu-id="bc4d0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc4d0-143">System.Boolean</span></span>

## <span data-ttu-id="bc4d0-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc4d0-144">NOTES</span></span>

<span data-ttu-id="bc4d0-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bc4d0-145">ALIASES</span></span>

<span data-ttu-id="bc4d0-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="bc4d0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc4d0-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc4d0-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc4d0-149">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="bc4d0-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc4d0-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="bc4d0-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="bc4d0-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="bc4d0-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="bc4d0-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="bc4d0-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc4d0-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="bc4d0-156">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="bc4d0-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="bc4d0-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bc4d0-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="bc4d0-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bc4d0-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc4d0-160">RELATED LINKS</span></span>

