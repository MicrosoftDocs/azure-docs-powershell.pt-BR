---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: e1b5a123d00e097e7e6315ac2231b145de645149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113047"
---
# <span data-ttu-id="ac75f-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="ac75f-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="ac75f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac75f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac75f-103">Adicione uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="ac75f-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ac75f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac75f-104">SYNTAX</span></span>

### <span data-ttu-id="ac75f-105">AddExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="ac75f-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac75f-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac75f-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac75f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac75f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac75f-108">Adicione uma lista de extensões de idioma que podem ser executados em consultas KQL.</span><span class="sxs-lookup"><span data-stu-id="ac75f-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="ac75f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac75f-109">EXAMPLES</span></span>

### <span data-ttu-id="ac75f-110">Exemplo 1: Adicionar uma lista de extensões de idioma</span><span class="sxs-lookup"><span data-stu-id="ac75f-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="ac75f-111">O comando acima adiciona uma lista de extensões de idioma que podem ser executados em consultas KQL</span><span class="sxs-lookup"><span data-stu-id="ac75f-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="ac75f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac75f-112">PARAMETERS</span></span>

### <span data-ttu-id="ac75f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac75f-113">-AsJob</span></span>
<span data-ttu-id="ac75f-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ac75f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ac75f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ac75f-115">-ClusterName</span></span>
<span data-ttu-id="ac75f-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="ac75f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ac75f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac75f-117">-DefaultProfile</span></span>
<span data-ttu-id="ac75f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac75f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac75f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac75f-119">-InputObject</span></span>
<span data-ttu-id="ac75f-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ac75f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac75f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac75f-121">-NoWait</span></span>
<span data-ttu-id="ac75f-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="ac75f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac75f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac75f-123">-PassThru</span></span>
<span data-ttu-id="ac75f-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ac75f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac75f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac75f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac75f-126">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="ac75f-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ac75f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac75f-127">-SubscriptionId</span></span>
<span data-ttu-id="ac75f-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac75f-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac75f-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ac75f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ac75f-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="ac75f-130">-Value</span></span>
<span data-ttu-id="ac75f-131">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="ac75f-131">The list of language extensions.</span></span>
<span data-ttu-id="ac75f-132">Para construir, confira a seção ANOTAÇÕES das propriedades VALOR e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ac75f-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac75f-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ac75f-133">-Confirm</span></span>
<span data-ttu-id="ac75f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac75f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac75f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac75f-135">-WhatIf</span></span>
<span data-ttu-id="ac75f-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ac75f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac75f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac75f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac75f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac75f-138">CommonParameters</span></span>
<span data-ttu-id="ac75f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac75f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac75f-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac75f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac75f-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="ac75f-141">INPUTS</span></span>

### <span data-ttu-id="ac75f-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ac75f-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ac75f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="ac75f-143">OUTPUTS</span></span>

### <span data-ttu-id="ac75f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac75f-144">System.Boolean</span></span>

## <span data-ttu-id="ac75f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="ac75f-145">NOTES</span></span>

<span data-ttu-id="ac75f-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="ac75f-146">ALIASES</span></span>

<span data-ttu-id="ac75f-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ac75f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac75f-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ac75f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac75f-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac75f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac75f-150">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="ac75f-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac75f-151">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="ac75f-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ac75f-152">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="ac75f-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ac75f-153">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ac75f-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ac75f-154">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="ac75f-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ac75f-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ac75f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac75f-156">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="ac75f-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ac75f-157">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ac75f-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ac75f-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="ac75f-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ac75f-159">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac75f-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ac75f-160">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ac75f-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ac75f-161">VALOR <ILanguageExtension[]>: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="ac75f-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ac75f-162">`[Name <LanguageExtensionName?>]`: o nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="ac75f-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="ac75f-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac75f-163">RELATED LINKS</span></span>

