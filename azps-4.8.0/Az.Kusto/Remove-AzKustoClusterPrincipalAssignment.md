---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954978"
---
# <span data-ttu-id="7a080-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7a080-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="7a080-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a080-102">SYNOPSIS</span></span>
<span data-ttu-id="7a080-103">Exclui um principalAssignment de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7a080-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a080-104">SYNTAX</span></span>

### <span data-ttu-id="7a080-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a080-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a080-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a080-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a080-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a080-107">DESCRIPTION</span></span>
<span data-ttu-id="7a080-108">Exclui um principalAssignment de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="7a080-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a080-109">EXAMPLES</span></span>

### <span data-ttu-id="7a080-110">Exemplo 1: excluir um cluster de Kusto existente PrincipalAssignment por nome</span><span class="sxs-lookup"><span data-stu-id="7a080-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="7a080-111">O comando acima exclui o PrincipalAssignment chamado "kustoprincipal1" no cluster Kusto "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7a080-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="7a080-112">OS</span><span class="sxs-lookup"><span data-stu-id="7a080-112">PARAMETERS</span></span>

### <span data-ttu-id="7a080-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a080-113">-AsJob</span></span>
<span data-ttu-id="7a080-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7a080-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7a080-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a080-115">-ClusterName</span></span>
<span data-ttu-id="7a080-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a080-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a080-117">-DefaultProfile</span></span>
<span data-ttu-id="7a080-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a080-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a080-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a080-119">-InputObject</span></span>
<span data-ttu-id="7a080-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7a080-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a080-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7a080-121">-NoWait</span></span>
<span data-ttu-id="7a080-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7a080-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a080-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a080-123">-PassThru</span></span>
<span data-ttu-id="7a080-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7a080-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7a080-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7a080-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="7a080-126">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-126">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="7a080-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a080-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a080-128">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a080-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a080-129">-SubscriptionId</span></span>
<span data-ttu-id="7a080-130">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a080-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7a080-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7a080-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7a080-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a080-132">-Confirm</span></span>
<span data-ttu-id="7a080-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a080-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a080-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a080-134">-WhatIf</span></span>
<span data-ttu-id="7a080-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a080-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a080-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a080-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a080-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a080-137">CommonParameters</span></span>
<span data-ttu-id="7a080-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a080-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a080-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a080-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a080-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a080-140">INPUTS</span></span>

### <span data-ttu-id="7a080-141">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7a080-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7a080-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a080-142">OUTPUTS</span></span>

### <span data-ttu-id="7a080-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a080-143">System.Boolean</span></span>

## <span data-ttu-id="7a080-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a080-144">NOTES</span></span>

<span data-ttu-id="7a080-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7a080-145">ALIASES</span></span>

<span data-ttu-id="7a080-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="7a080-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a080-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7a080-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a080-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a080-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a080-149">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7a080-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a080-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="7a080-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7a080-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7a080-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="7a080-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7a080-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7a080-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7a080-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a080-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a080-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7a080-156">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7a080-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7a080-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7a080-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a080-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7a080-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7a080-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7a080-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a080-160">RELATED LINKS</span></span>

