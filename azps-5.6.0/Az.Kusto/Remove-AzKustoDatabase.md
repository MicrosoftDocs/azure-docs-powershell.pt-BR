---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: ab6ef84d05e77711a767f35f915d53c2fe5cdb46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888358"
---
# <span data-ttu-id="64af2-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="64af2-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="64af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64af2-102">SYNOPSIS</span></span>
<span data-ttu-id="64af2-103">Exclui o banco de dados com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="64af2-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="64af2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="64af2-104">SYNTAX</span></span>

### <span data-ttu-id="64af2-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="64af2-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64af2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64af2-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64af2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="64af2-107">DESCRIPTION</span></span>
<span data-ttu-id="64af2-108">Exclui o banco de dados com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="64af2-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="64af2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64af2-109">EXAMPLES</span></span>

### <span data-ttu-id="64af2-110">Exemplo 1: Excluir um banco de dados Kusto existente pelo nome</span><span class="sxs-lookup"><span data-stu-id="64af2-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="64af2-111">O comando acima exclui o banco de dados Kusto chamado "mykustodatabase" no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="64af2-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="64af2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="64af2-112">PARAMETERS</span></span>

### <span data-ttu-id="64af2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64af2-113">-AsJob</span></span>
<span data-ttu-id="64af2-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="64af2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="64af2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64af2-115">-ClusterName</span></span>
<span data-ttu-id="64af2-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="64af2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64af2-117">-DefaultProfile</span></span>
<span data-ttu-id="64af2-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64af2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64af2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64af2-119">-InputObject</span></span>
<span data-ttu-id="64af2-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="64af2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64af2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64af2-121">-Name</span></span>
<span data-ttu-id="64af2-122">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-122">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="64af2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64af2-123">-NoWait</span></span>
<span data-ttu-id="64af2-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="64af2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64af2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64af2-125">-PassThru</span></span>
<span data-ttu-id="64af2-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="64af2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64af2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64af2-127">-ResourceGroupName</span></span>
<span data-ttu-id="64af2-128">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="64af2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64af2-129">-SubscriptionId</span></span>
<span data-ttu-id="64af2-130">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64af2-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64af2-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="64af2-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64af2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64af2-132">-Confirm</span></span>
<span data-ttu-id="64af2-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64af2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64af2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64af2-134">-WhatIf</span></span>
<span data-ttu-id="64af2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64af2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64af2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64af2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64af2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64af2-137">CommonParameters</span></span>
<span data-ttu-id="64af2-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64af2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64af2-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64af2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64af2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64af2-140">INPUTS</span></span>

### <span data-ttu-id="64af2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="64af2-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="64af2-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="64af2-142">OUTPUTS</span></span>

### <span data-ttu-id="64af2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64af2-143">System.Boolean</span></span>

## <span data-ttu-id="64af2-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="64af2-144">NOTES</span></span>

<span data-ttu-id="64af2-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64af2-145">ALIASES</span></span>

<span data-ttu-id="64af2-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="64af2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64af2-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="64af2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64af2-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64af2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64af2-149">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="64af2-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64af2-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="64af2-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="64af2-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="64af2-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="64af2-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="64af2-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="64af2-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="64af2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64af2-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="64af2-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="64af2-156">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="64af2-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="64af2-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="64af2-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="64af2-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64af2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64af2-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="64af2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="64af2-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64af2-160">RELATED LINKS</span></span>

