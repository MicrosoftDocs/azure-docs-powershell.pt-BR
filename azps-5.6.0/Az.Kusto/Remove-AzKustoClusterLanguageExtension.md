---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 6a687139f7dec156e539c09b864a88c4e8876fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887989"
---
# <span data-ttu-id="eaf8e-101">Remove-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="eaf8e-101">Remove-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="eaf8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf8e-103">Remova uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-103">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="eaf8e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eaf8e-104">SYNTAX</span></span>

### <span data-ttu-id="eaf8e-105">RemoveExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eaf8e-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eaf8e-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eaf8e-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eaf8e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eaf8e-107">DESCRIPTION</span></span>
<span data-ttu-id="eaf8e-108">Remova uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-108">Remove a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="eaf8e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-109">EXAMPLES</span></span>

### <span data-ttu-id="eaf8e-110">Exemplo 1: Remover uma lista de extensões de idioma do cluster</span><span class="sxs-lookup"><span data-stu-id="eaf8e-110">Example 1: Remove a list of language extensions from cluster</span></span>
```powershell
PS C:\> Remove-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"})
```

<span data-ttu-id="eaf8e-111">O comando acima remove uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-111">The above command removes a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="eaf8e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-112">PARAMETERS</span></span>

### <span data-ttu-id="eaf8e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaf8e-113">-AsJob</span></span>
<span data-ttu-id="eaf8e-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="eaf8e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="eaf8e-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eaf8e-115">-ClusterName</span></span>
<span data-ttu-id="eaf8e-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="eaf8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf8e-117">-DefaultProfile</span></span>
<span data-ttu-id="eaf8e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eaf8e-119">-InputObject</span></span>
<span data-ttu-id="eaf8e-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eaf8e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eaf8e-121">-NoWait</span></span>
<span data-ttu-id="eaf8e-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="eaf8e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eaf8e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaf8e-123">-PassThru</span></span>
<span data-ttu-id="eaf8e-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="eaf8e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eaf8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="eaf8e-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="eaf8e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eaf8e-127">-SubscriptionId</span></span>
<span data-ttu-id="eaf8e-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eaf8e-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eaf8e-130">-Value</span><span class="sxs-lookup"><span data-stu-id="eaf8e-130">-Value</span></span>
<span data-ttu-id="eaf8e-131">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-131">The list of language extensions.</span></span>
<span data-ttu-id="eaf8e-132">Para construir, consulte a seção NOTES para propriedades VALUE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf8e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf8e-133">-Confirm</span></span>
<span data-ttu-id="eaf8e-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf8e-135">-WhatIf</span></span>
<span data-ttu-id="eaf8e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf8e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf8e-138">CommonParameters</span></span>
<span data-ttu-id="eaf8e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf8e-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaf8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf8e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-141">INPUTS</span></span>

### <span data-ttu-id="eaf8e-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="eaf8e-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="eaf8e-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-143">OUTPUTS</span></span>

### <span data-ttu-id="eaf8e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eaf8e-144">System.Boolean</span></span>

## <span data-ttu-id="eaf8e-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="eaf8e-145">NOTES</span></span>

<span data-ttu-id="eaf8e-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="eaf8e-146">ALIASES</span></span>

<span data-ttu-id="eaf8e-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="eaf8e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eaf8e-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eaf8e-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eaf8e-150">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="eaf8e-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eaf8e-151">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="eaf8e-152">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="eaf8e-153">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="eaf8e-154">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="eaf8e-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="eaf8e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eaf8e-156">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="eaf8e-157">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="eaf8e-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="eaf8e-159">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eaf8e-160">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="eaf8e-161">VALUE <ILanguageExtension[]>: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="eaf8e-162">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="eaf8e-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="eaf8e-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eaf8e-163">RELATED LINKS</span></span>

