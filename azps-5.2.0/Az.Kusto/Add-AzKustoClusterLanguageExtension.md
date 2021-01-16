---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262858"
---
# <span data-ttu-id="c7bb9-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="c7bb9-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="c7bb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bb9-103">Adicione uma lista de extensões de idioma que podem ser executadas em consultas do KQL.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c7bb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7bb9-104">SYNTAX</span></span>

### <span data-ttu-id="c7bb9-105">Addexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7bb9-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7bb9-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7bb9-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7bb9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="c7bb9-108">Adicione uma lista de extensões de idioma que podem ser executadas em consultas do KQL.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c7bb9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7bb9-109">EXAMPLES</span></span>

### <span data-ttu-id="c7bb9-110">Exemplo 1: adicionar uma lista de extensões de idioma</span><span class="sxs-lookup"><span data-stu-id="c7bb9-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="c7bb9-111">O comando acima adiciona uma lista de extensões de idioma que podem ser executadas em consultas do KQL</span><span class="sxs-lookup"><span data-stu-id="c7bb9-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="c7bb9-112">OS</span><span class="sxs-lookup"><span data-stu-id="c7bb9-112">PARAMETERS</span></span>

### <span data-ttu-id="c7bb9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7bb9-113">-AsJob</span></span>
<span data-ttu-id="c7bb9-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c7bb9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c7bb9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c7bb9-115">-ClusterName</span></span>
<span data-ttu-id="c7bb9-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bb9-117">-DefaultProfile</span></span>
<span data-ttu-id="c7bb9-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7bb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7bb9-119">-InputObject</span></span>
<span data-ttu-id="c7bb9-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bb9-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c7bb9-121">-NoWait</span></span>
<span data-ttu-id="c7bb9-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c7bb9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7bb9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7bb9-123">-PassThru</span></span>
<span data-ttu-id="c7bb9-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c7bb9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c7bb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7bb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7bb9-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bb9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7bb9-127">-SubscriptionId</span></span>
<span data-ttu-id="c7bb9-128">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c7bb9-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bb9-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="c7bb9-130">-Value</span></span>
<span data-ttu-id="c7bb9-131">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-131">The list of language extensions.</span></span>
<span data-ttu-id="c7bb9-132">Para construir, consulte a seção observações para propriedades de valor e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7bb9-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7bb9-133">-Confirm</span></span>
<span data-ttu-id="c7bb9-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bb9-135">-WhatIf</span></span>
<span data-ttu-id="c7bb9-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7bb9-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bb9-138">CommonParameters</span></span>
<span data-ttu-id="c7bb9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bb9-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7bb9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bb9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7bb9-141">INPUTS</span></span>

### <span data-ttu-id="c7bb9-142">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c7bb9-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c7bb9-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7bb9-143">OUTPUTS</span></span>

### <span data-ttu-id="c7bb9-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7bb9-144">System.Boolean</span></span>

## <span data-ttu-id="c7bb9-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7bb9-145">NOTES</span></span>

<span data-ttu-id="c7bb9-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c7bb9-146">ALIASES</span></span>

<span data-ttu-id="c7bb9-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c7bb9-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7bb9-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7bb9-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7bb9-150">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c7bb9-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7bb9-151">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c7bb9-152">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c7bb9-153">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c7bb9-154">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c7bb9-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c7bb9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7bb9-156">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c7bb9-157">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c7bb9-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c7bb9-159">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c7bb9-160">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="c7bb9-161">VALOR <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="c7bb9-162">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="c7bb9-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="c7bb9-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7bb9-163">RELATED LINKS</span></span>

