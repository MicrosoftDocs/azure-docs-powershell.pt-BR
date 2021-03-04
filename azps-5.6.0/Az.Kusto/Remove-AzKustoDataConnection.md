---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: ac2eac129231f33a2f74732923652d3851debbd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888240"
---
# <span data-ttu-id="ae139-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="ae139-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="ae139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae139-102">SYNOPSIS</span></span>
<span data-ttu-id="ae139-103">Exclui a conexão de dados com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="ae139-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="ae139-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae139-104">SYNTAX</span></span>

### <span data-ttu-id="ae139-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae139-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae139-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ae139-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae139-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae139-107">DESCRIPTION</span></span>
<span data-ttu-id="ae139-108">Exclui a conexão de dados com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="ae139-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="ae139-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae139-109">EXAMPLES</span></span>

### <span data-ttu-id="ae139-110">Exemplo 1: Excluir uma conexão de dados existente pelo nome</span><span class="sxs-lookup"><span data-stu-id="ae139-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="ae139-111">O comando acima exclui a conexão de dados chamada "mykustodataconnection" no banco de dados "mykustodatabase" do cluster existente "testnewkustocluster" encontrado no grupo de recursos "testrg"</span><span class="sxs-lookup"><span data-stu-id="ae139-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="ae139-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae139-112">PARAMETERS</span></span>

### <span data-ttu-id="ae139-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae139-113">-AsJob</span></span>
<span data-ttu-id="ae139-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ae139-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ae139-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ae139-115">-ClusterName</span></span>
<span data-ttu-id="ae139-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae139-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae139-117">-DatabaseName</span></span>
<span data-ttu-id="ae139-118">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae139-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae139-119">-DefaultProfile</span></span>
<span data-ttu-id="ae139-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae139-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae139-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae139-121">-InputObject</span></span>
<span data-ttu-id="ae139-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ae139-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae139-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ae139-123">-Name</span></span>
<span data-ttu-id="ae139-124">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ae139-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae139-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae139-125">-NoWait</span></span>
<span data-ttu-id="ae139-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ae139-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae139-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae139-127">-PassThru</span></span>
<span data-ttu-id="ae139-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ae139-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ae139-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae139-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae139-130">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ae139-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae139-131">-SubscriptionId</span></span>
<span data-ttu-id="ae139-132">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae139-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae139-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ae139-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ae139-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae139-134">-Confirm</span></span>
<span data-ttu-id="ae139-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae139-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae139-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae139-136">-WhatIf</span></span>
<span data-ttu-id="ae139-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae139-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae139-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae139-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae139-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae139-139">CommonParameters</span></span>
<span data-ttu-id="ae139-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae139-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae139-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae139-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae139-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae139-142">INPUTS</span></span>

### <span data-ttu-id="ae139-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ae139-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ae139-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae139-144">OUTPUTS</span></span>

### <span data-ttu-id="ae139-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae139-145">System.Boolean</span></span>

## <span data-ttu-id="ae139-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae139-146">NOTES</span></span>

<span data-ttu-id="ae139-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae139-147">ALIASES</span></span>

<span data-ttu-id="ae139-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ae139-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae139-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ae139-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae139-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae139-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae139-151">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ae139-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae139-152">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="ae139-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ae139-153">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ae139-154">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ae139-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ae139-155">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ae139-156">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ae139-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae139-157">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae139-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ae139-158">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ae139-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ae139-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ae139-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ae139-160">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae139-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ae139-161">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ae139-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ae139-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae139-162">RELATED LINKS</span></span>

