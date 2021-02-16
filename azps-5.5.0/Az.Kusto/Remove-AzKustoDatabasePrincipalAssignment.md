---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117588"
---
# <span data-ttu-id="10e34-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="10e34-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="10e34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10e34-102">SYNOPSIS</span></span>
<span data-ttu-id="10e34-103">Exclui um Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="10e34-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="10e34-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10e34-104">SYNTAX</span></span>

### <span data-ttu-id="10e34-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10e34-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10e34-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10e34-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10e34-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="10e34-107">DESCRIPTION</span></span>
<span data-ttu-id="10e34-108">Exclui um Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="10e34-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="10e34-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10e34-109">EXAMPLES</span></span>

### <span data-ttu-id="10e34-110">Exemplo 1: Excluir um nome de banco de dados do Kusto existente</span><span class="sxs-lookup"><span data-stu-id="10e34-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="10e34-111">O comando acima exclui o principalAssignment chamado "kustoprincipal1" no banco de dados de Kusto "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="10e34-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="10e34-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10e34-112">PARAMETERS</span></span>

### <span data-ttu-id="10e34-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10e34-113">-AsJob</span></span>
<span data-ttu-id="10e34-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="10e34-114">Run the command as a job</span></span>

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

### <span data-ttu-id="10e34-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="10e34-115">-ClusterName</span></span>
<span data-ttu-id="10e34-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="10e34-117">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="10e34-117">-DatabaseName</span></span>
<span data-ttu-id="10e34-118">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="10e34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e34-119">-DefaultProfile</span></span>
<span data-ttu-id="10e34-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10e34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10e34-121">-InputObject</span></span>
<span data-ttu-id="10e34-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="10e34-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10e34-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="10e34-123">-NoWait</span></span>
<span data-ttu-id="10e34-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="10e34-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="10e34-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10e34-125">-PassThru</span></span>
<span data-ttu-id="10e34-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="10e34-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="10e34-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="10e34-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="10e34-128">O nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="10e34-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="10e34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e34-129">-ResourceGroupName</span></span>
<span data-ttu-id="10e34-130">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="10e34-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10e34-131">-SubscriptionId</span></span>
<span data-ttu-id="10e34-132">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10e34-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="10e34-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="10e34-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="10e34-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10e34-134">-Confirm</span></span>
<span data-ttu-id="10e34-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e34-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e34-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e34-136">-WhatIf</span></span>
<span data-ttu-id="10e34-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10e34-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e34-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10e34-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e34-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e34-139">CommonParameters</span></span>
<span data-ttu-id="10e34-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e34-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e34-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e34-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e34-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="10e34-142">INPUTS</span></span>

### <span data-ttu-id="10e34-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="10e34-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="10e34-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="10e34-144">OUTPUTS</span></span>

### <span data-ttu-id="10e34-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10e34-145">System.Boolean</span></span>

## <span data-ttu-id="10e34-146">Notas</span><span class="sxs-lookup"><span data-stu-id="10e34-146">NOTES</span></span>

<span data-ttu-id="10e34-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="10e34-147">ALIASES</span></span>

<span data-ttu-id="10e34-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="10e34-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10e34-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="10e34-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10e34-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10e34-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10e34-151">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="10e34-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10e34-152">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="10e34-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="10e34-153">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="10e34-154">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="10e34-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="10e34-155">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="10e34-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="10e34-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10e34-157">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="10e34-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="10e34-158">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="10e34-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="10e34-159">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="10e34-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="10e34-160">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10e34-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="10e34-161">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="10e34-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="10e34-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10e34-162">RELATED LINKS</span></span>

