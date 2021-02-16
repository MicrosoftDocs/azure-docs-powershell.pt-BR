---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113625"
---
# <span data-ttu-id="f346a-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="f346a-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="f346a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f346a-102">SYNOPSIS</span></span>
<span data-ttu-id="f346a-103">Exclui a configuração de banco de dados anexada com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="f346a-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="f346a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f346a-104">SYNTAX</span></span>

### <span data-ttu-id="f346a-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f346a-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f346a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f346a-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f346a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f346a-107">DESCRIPTION</span></span>
<span data-ttu-id="f346a-108">Exclui a configuração de banco de dados anexada com o nome determinado.</span><span class="sxs-lookup"><span data-stu-id="f346a-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="f346a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f346a-109">EXAMPLES</span></span>

### <span data-ttu-id="f346a-110">Exemplo 1: Excluir um nome de AttachedDatabaseConfiguration existente</span><span class="sxs-lookup"><span data-stu-id="f346a-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="f346a-111">O comando acima exclui o banco de dados de seguidores definido na attachedDatabaseConfiguration "myfollowerconfiguration" do cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="f346a-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="f346a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f346a-112">PARAMETERS</span></span>

### <span data-ttu-id="f346a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f346a-113">-AsJob</span></span>
<span data-ttu-id="f346a-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f346a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f346a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f346a-115">-ClusterName</span></span>
<span data-ttu-id="f346a-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="f346a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f346a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f346a-117">-DefaultProfile</span></span>
<span data-ttu-id="f346a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f346a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f346a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f346a-119">-InputObject</span></span>
<span data-ttu-id="f346a-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f346a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f346a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f346a-121">-Name</span></span>
<span data-ttu-id="f346a-122">O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f346a-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f346a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f346a-123">-NoWait</span></span>
<span data-ttu-id="f346a-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="f346a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f346a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f346a-125">-PassThru</span></span>
<span data-ttu-id="f346a-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f346a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f346a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f346a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f346a-128">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="f346a-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f346a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f346a-129">-SubscriptionId</span></span>
<span data-ttu-id="f346a-130">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f346a-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f346a-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f346a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f346a-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f346a-132">-Confirm</span></span>
<span data-ttu-id="f346a-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f346a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f346a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f346a-134">-WhatIf</span></span>
<span data-ttu-id="f346a-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f346a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f346a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f346a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f346a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f346a-137">CommonParameters</span></span>
<span data-ttu-id="f346a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f346a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f346a-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f346a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f346a-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="f346a-140">INPUTS</span></span>

### <span data-ttu-id="f346a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f346a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f346a-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="f346a-142">OUTPUTS</span></span>

### <span data-ttu-id="f346a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f346a-143">System.Boolean</span></span>

## <span data-ttu-id="f346a-144">Notas</span><span class="sxs-lookup"><span data-stu-id="f346a-144">NOTES</span></span>

<span data-ttu-id="f346a-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="f346a-145">ALIASES</span></span>

<span data-ttu-id="f346a-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f346a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f346a-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f346a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f346a-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f346a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f346a-149">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f346a-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f346a-150">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f346a-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f346a-151">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="f346a-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f346a-152">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="f346a-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f346a-153">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="f346a-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f346a-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f346a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f346a-155">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="f346a-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f346a-156">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f346a-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f346a-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="f346a-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f346a-158">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f346a-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f346a-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f346a-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f346a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f346a-160">RELATED LINKS</span></span>

