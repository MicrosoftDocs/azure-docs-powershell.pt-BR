---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124915"
---
# <span data-ttu-id="cda32-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cda32-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="cda32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cda32-102">SYNOPSIS</span></span>
<span data-ttu-id="cda32-103">Exclui um Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cda32-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="cda32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cda32-104">SYNTAX</span></span>

### <span data-ttu-id="cda32-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="cda32-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cda32-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cda32-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cda32-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cda32-107">DESCRIPTION</span></span>
<span data-ttu-id="cda32-108">Exclui um Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cda32-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="cda32-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cda32-109">EXAMPLES</span></span>

### <span data-ttu-id="cda32-110">Exemplo 1: excluir um banco de dados do Kusto existente PrincipalAssignment por nome</span><span class="sxs-lookup"><span data-stu-id="cda32-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="cda32-111">O comando acima exclui o PrincipalAssignment chamado "kustoprincipal1" no banco de dados do Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="cda32-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="cda32-112">OS</span><span class="sxs-lookup"><span data-stu-id="cda32-112">PARAMETERS</span></span>

### <span data-ttu-id="cda32-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cda32-113">-AsJob</span></span>
<span data-ttu-id="cda32-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cda32-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cda32-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cda32-115">-ClusterName</span></span>
<span data-ttu-id="cda32-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cda32-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cda32-117">-DatabaseName</span></span>
<span data-ttu-id="cda32-118">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cda32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda32-119">-DefaultProfile</span></span>
<span data-ttu-id="cda32-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cda32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda32-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cda32-121">-InputObject</span></span>
<span data-ttu-id="cda32-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cda32-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cda32-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cda32-123">-NoWait</span></span>
<span data-ttu-id="cda32-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cda32-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cda32-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cda32-125">-PassThru</span></span>
<span data-ttu-id="cda32-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cda32-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cda32-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cda32-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="cda32-128">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="cda32-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda32-129">-ResourceGroupName</span></span>
<span data-ttu-id="cda32-130">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cda32-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cda32-131">-SubscriptionId</span></span>
<span data-ttu-id="cda32-132">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cda32-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cda32-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cda32-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cda32-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cda32-134">-Confirm</span></span>
<span data-ttu-id="cda32-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cda32-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda32-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda32-136">-WhatIf</span></span>
<span data-ttu-id="cda32-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cda32-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda32-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cda32-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda32-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda32-139">CommonParameters</span></span>
<span data-ttu-id="cda32-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda32-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda32-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cda32-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda32-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cda32-142">INPUTS</span></span>

### <span data-ttu-id="cda32-143">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cda32-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cda32-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cda32-144">OUTPUTS</span></span>

### <span data-ttu-id="cda32-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cda32-145">System.Boolean</span></span>

## <span data-ttu-id="cda32-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cda32-146">NOTES</span></span>

<span data-ttu-id="cda32-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cda32-147">ALIASES</span></span>

<span data-ttu-id="cda32-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="cda32-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cda32-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cda32-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cda32-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cda32-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cda32-151">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="cda32-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cda32-152">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="cda32-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cda32-153">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cda32-154">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="cda32-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cda32-155">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cda32-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cda32-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cda32-157">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="cda32-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cda32-158">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cda32-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cda32-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cda32-160">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cda32-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cda32-161">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cda32-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cda32-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cda32-162">RELATED LINKS</span></span>

