---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: e9bdea3820b8b8121e0e250c99283c0ca656ca61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113746"
---
# <span data-ttu-id="8f9ba-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8f9ba-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="8f9ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9ba-103">Exclui um cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="8f9ba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f9ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f9ba-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f9ba-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f9ba-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f9ba-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f9ba-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f9ba-107">DESCRIPTION</span></span>
<span data-ttu-id="8f9ba-108">Exclui um cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="8f9ba-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f9ba-109">EXAMPLES</span></span>

### <span data-ttu-id="8f9ba-110">Exemplo 1: Excluir um cluster Kusto existente por nome</span><span class="sxs-lookup"><span data-stu-id="8f9ba-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="8f9ba-111">O comando acima exclui o cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="8f9ba-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="8f9ba-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f9ba-112">PARAMETERS</span></span>

### <span data-ttu-id="8f9ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f9ba-113">-AsJob</span></span>
<span data-ttu-id="8f9ba-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8f9ba-114">Run the command as a job</span></span>

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

### <span data-ttu-id="8f9ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9ba-115">-DefaultProfile</span></span>
<span data-ttu-id="8f9ba-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f9ba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f9ba-117">-InputObject</span></span>
<span data-ttu-id="8f9ba-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f9ba-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f9ba-119">-Name</span></span>
<span data-ttu-id="8f9ba-120">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8f9ba-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f9ba-121">-NoWait</span></span>
<span data-ttu-id="8f9ba-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="8f9ba-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f9ba-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f9ba-123">-PassThru</span></span>
<span data-ttu-id="8f9ba-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8f9ba-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8f9ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f9ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f9ba-126">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8f9ba-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f9ba-127">-SubscriptionId</span></span>
<span data-ttu-id="8f9ba-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f9ba-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8f9ba-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f9ba-130">-Confirm</span></span>
<span data-ttu-id="8f9ba-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f9ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f9ba-132">-WhatIf</span></span>
<span data-ttu-id="8f9ba-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f9ba-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f9ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9ba-135">CommonParameters</span></span>
<span data-ttu-id="8f9ba-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9ba-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f9ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9ba-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f9ba-138">INPUTS</span></span>

### <span data-ttu-id="8f9ba-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8f9ba-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8f9ba-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f9ba-140">OUTPUTS</span></span>

### <span data-ttu-id="8f9ba-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f9ba-141">System.Boolean</span></span>

## <span data-ttu-id="8f9ba-142">Notas</span><span class="sxs-lookup"><span data-stu-id="8f9ba-142">NOTES</span></span>

<span data-ttu-id="8f9ba-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="8f9ba-143">ALIASES</span></span>

<span data-ttu-id="8f9ba-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8f9ba-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f9ba-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f9ba-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f9ba-147">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8f9ba-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f9ba-148">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8f9ba-149">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8f9ba-150">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8f9ba-151">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8f9ba-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8f9ba-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f9ba-153">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8f9ba-154">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8f9ba-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8f9ba-156">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8f9ba-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8f9ba-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f9ba-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f9ba-158">RELATED LINKS</span></span>

