---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: bd643f5a655819179646d30bcee1b96f1509df17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954979"
---
# <span data-ttu-id="69093-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="69093-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="69093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69093-102">SYNOPSIS</span></span>
<span data-ttu-id="69093-103">Remova uma lista de extensões de idioma que podem ser executadas em consultas do KQL.</span><span class="sxs-lookup"><span data-stu-id="69093-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="69093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69093-104">SYNTAX</span></span>

### <span data-ttu-id="69093-105">RemoveExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="69093-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69093-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69093-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69093-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69093-107">DESCRIPTION</span></span>
<span data-ttu-id="69093-108">Remova uma lista de extensões de idioma que podem ser executadas em consultas do KQL.</span><span class="sxs-lookup"><span data-stu-id="69093-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="69093-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69093-109">EXAMPLES</span></span>

### <span data-ttu-id="69093-110">Exemplo 1: remover uma lista de extensões de idioma do cluster</span><span class="sxs-lookup"><span data-stu-id="69093-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="69093-111">O comando acima remove uma lista de extensões de idioma que podem ser executadas em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="69093-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="69093-112">OS</span><span class="sxs-lookup"><span data-stu-id="69093-112">PARAMETERS</span></span>

### <span data-ttu-id="69093-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69093-113">-AsJob</span></span>
<span data-ttu-id="69093-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="69093-114">Run the command as a job</span></span>

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

### <span data-ttu-id="69093-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="69093-115">-ClusterName</span></span>
<span data-ttu-id="69093-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69093-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69093-117">-DefaultProfile</span></span>
<span data-ttu-id="69093-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69093-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69093-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69093-119">-InputObject</span></span>
<span data-ttu-id="69093-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="69093-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69093-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="69093-121">-NoWait</span></span>
<span data-ttu-id="69093-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="69093-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69093-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69093-123">-PassThru</span></span>
<span data-ttu-id="69093-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="69093-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69093-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69093-125">-ResourceGroupName</span></span>
<span data-ttu-id="69093-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69093-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69093-127">-SubscriptionId</span></span>
<span data-ttu-id="69093-128">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69093-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="69093-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="69093-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69093-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="69093-130">-Value</span></span>
<span data-ttu-id="69093-131">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="69093-131">The list of language extensions.</span></span>
<span data-ttu-id="69093-132">Para construir, consulte a seção observações para propriedades de valor e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="69093-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69093-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69093-133">-Confirm</span></span>
<span data-ttu-id="69093-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69093-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69093-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69093-135">-WhatIf</span></span>
<span data-ttu-id="69093-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69093-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69093-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69093-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69093-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69093-138">CommonParameters</span></span>
<span data-ttu-id="69093-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69093-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69093-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69093-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69093-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69093-141">INPUTS</span></span>

### <span data-ttu-id="69093-142">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="69093-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="69093-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69093-143">OUTPUTS</span></span>

### <span data-ttu-id="69093-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69093-144">System.Boolean</span></span>

## <span data-ttu-id="69093-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69093-145">NOTES</span></span>

<span data-ttu-id="69093-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="69093-146">ALIASES</span></span>

<span data-ttu-id="69093-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="69093-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69093-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="69093-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69093-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69093-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69093-150">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="69093-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69093-151">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="69093-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="69093-152">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="69093-153">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="69093-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="69093-154">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="69093-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="69093-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69093-156">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="69093-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="69093-157">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="69093-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="69093-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="69093-159">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69093-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="69093-160">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="69093-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="69093-161">VALOR <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="69093-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="69093-162">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="69093-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="69093-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69093-163">RELATED LINKS</span></span>

