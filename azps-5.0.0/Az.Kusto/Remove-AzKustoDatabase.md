---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124918"
---
# <span data-ttu-id="c40c8-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="c40c8-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="c40c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c40c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c40c8-103">Exclui o banco de dados com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="c40c8-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="c40c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c40c8-104">SYNTAX</span></span>

### <span data-ttu-id="c40c8-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="c40c8-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c40c8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c40c8-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c40c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c40c8-107">DESCRIPTION</span></span>
<span data-ttu-id="c40c8-108">Exclui o banco de dados com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="c40c8-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="c40c8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c40c8-109">EXAMPLES</span></span>

### <span data-ttu-id="c40c8-110">Exemplo 1: excluir um banco de dados do Kusto existente por nome</span><span class="sxs-lookup"><span data-stu-id="c40c8-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="c40c8-111">O comando acima exclui o banco de dados Kusto chamado "mykustodatabase" no cluster "testnewkustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="c40c8-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c40c8-112">OS</span><span class="sxs-lookup"><span data-stu-id="c40c8-112">PARAMETERS</span></span>

### <span data-ttu-id="c40c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c40c8-113">-AsJob</span></span>
<span data-ttu-id="c40c8-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c40c8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c40c8-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c40c8-115">-ClusterName</span></span>
<span data-ttu-id="c40c8-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c40c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40c8-117">-DefaultProfile</span></span>
<span data-ttu-id="c40c8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c40c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c40c8-119">-InputObject</span></span>
<span data-ttu-id="c40c8-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c40c8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c40c8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c40c8-121">-Name</span></span>
<span data-ttu-id="c40c8-122">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40c8-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c40c8-123">-NoWait</span></span>
<span data-ttu-id="c40c8-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c40c8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c40c8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c40c8-125">-PassThru</span></span>
<span data-ttu-id="c40c8-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c40c8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c40c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="c40c8-128">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c40c8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c40c8-129">-SubscriptionId</span></span>
<span data-ttu-id="c40c8-130">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c40c8-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c40c8-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c40c8-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c40c8-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c40c8-132">-Confirm</span></span>
<span data-ttu-id="c40c8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c40c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c40c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40c8-134">-WhatIf</span></span>
<span data-ttu-id="c40c8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c40c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40c8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c40c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c40c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40c8-137">CommonParameters</span></span>
<span data-ttu-id="c40c8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40c8-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c40c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40c8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c40c8-140">INPUTS</span></span>

### <span data-ttu-id="c40c8-141">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c40c8-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c40c8-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c40c8-142">OUTPUTS</span></span>

### <span data-ttu-id="c40c8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c40c8-143">System.Boolean</span></span>

## <span data-ttu-id="c40c8-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c40c8-144">NOTES</span></span>

<span data-ttu-id="c40c8-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c40c8-145">ALIASES</span></span>

<span data-ttu-id="c40c8-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c40c8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c40c8-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c40c8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c40c8-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c40c8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c40c8-149">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c40c8-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c40c8-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="c40c8-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c40c8-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c40c8-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c40c8-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c40c8-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c40c8-154">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c40c8-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c40c8-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="c40c8-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c40c8-156">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c40c8-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c40c8-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c40c8-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c40c8-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c40c8-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c40c8-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c40c8-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c40c8-160">RELATED LINKS</span></span>

