---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 90d080f3c45db107c3f7f86ed8c32c3efe0b066c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886022"
---
# <span data-ttu-id="25a52-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="25a52-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="25a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a52-102">SYNOPSIS</span></span>
<span data-ttu-id="25a52-103">Exclui um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="25a52-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="25a52-104">SYNTAX</span></span>

### <span data-ttu-id="25a52-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25a52-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25a52-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25a52-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25a52-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="25a52-107">DESCRIPTION</span></span>
<span data-ttu-id="25a52-108">Exclui um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="25a52-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25a52-109">EXAMPLES</span></span>

### <span data-ttu-id="25a52-110">Exemplo 1: Excluir um cluster Kusto existente pelo nome</span><span class="sxs-lookup"><span data-stu-id="25a52-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="25a52-111">O comando acima exclui o cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="25a52-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="25a52-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="25a52-112">PARAMETERS</span></span>

### <span data-ttu-id="25a52-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25a52-113">-AsJob</span></span>
<span data-ttu-id="25a52-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="25a52-114">Run the command as a job</span></span>

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

### <span data-ttu-id="25a52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a52-115">-DefaultProfile</span></span>
<span data-ttu-id="25a52-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25a52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a52-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25a52-117">-InputObject</span></span>
<span data-ttu-id="25a52-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="25a52-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25a52-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25a52-119">-Name</span></span>
<span data-ttu-id="25a52-120">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a52-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25a52-121">-NoWait</span></span>
<span data-ttu-id="25a52-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="25a52-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25a52-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25a52-123">-PassThru</span></span>
<span data-ttu-id="25a52-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="25a52-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25a52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a52-125">-ResourceGroupName</span></span>
<span data-ttu-id="25a52-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="25a52-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25a52-127">-SubscriptionId</span></span>
<span data-ttu-id="25a52-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25a52-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25a52-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25a52-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25a52-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25a52-130">-Confirm</span></span>
<span data-ttu-id="25a52-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25a52-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a52-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a52-132">-WhatIf</span></span>
<span data-ttu-id="25a52-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25a52-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25a52-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25a52-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a52-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a52-135">CommonParameters</span></span>
<span data-ttu-id="25a52-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a52-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a52-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25a52-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a52-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25a52-138">INPUTS</span></span>

### <span data-ttu-id="25a52-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="25a52-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="25a52-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="25a52-140">OUTPUTS</span></span>

### <span data-ttu-id="25a52-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25a52-141">System.Boolean</span></span>

## <span data-ttu-id="25a52-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="25a52-142">NOTES</span></span>

<span data-ttu-id="25a52-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25a52-143">ALIASES</span></span>

<span data-ttu-id="25a52-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="25a52-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25a52-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="25a52-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25a52-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25a52-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25a52-147">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="25a52-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25a52-148">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="25a52-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="25a52-149">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="25a52-150">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="25a52-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="25a52-151">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="25a52-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="25a52-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25a52-153">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="25a52-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="25a52-154">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="25a52-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="25a52-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="25a52-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="25a52-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25a52-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25a52-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25a52-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="25a52-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25a52-158">RELATED LINKS</span></span>

