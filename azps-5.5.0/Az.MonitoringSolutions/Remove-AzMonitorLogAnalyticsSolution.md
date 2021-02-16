---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113551"
---
# <span data-ttu-id="12fc3-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="12fc3-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="12fc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="12fc3-103">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="12fc3-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="12fc3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12fc3-104">SYNTAX</span></span>

### <span data-ttu-id="12fc3-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12fc3-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12fc3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12fc3-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12fc3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="12fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="12fc3-108">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="12fc3-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="12fc3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="12fc3-110">Exemplo 1: remover uma solução de análise de log de monitor por nome</span><span class="sxs-lookup"><span data-stu-id="12fc3-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="12fc3-111">Esse comando remove uma solução de análise de log de monitor por nome.</span><span class="sxs-lookup"><span data-stu-id="12fc3-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="12fc3-112">Exemplo 2: remover uma solução de análise de log de monitor por objeto</span><span class="sxs-lookup"><span data-stu-id="12fc3-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="12fc3-113">Esse comando remove uma solução de análise de log de monitor por objeto.</span><span class="sxs-lookup"><span data-stu-id="12fc3-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="12fc3-114">Exemplo 3: remover uma solução de análise de log de monitor por pipeline</span><span class="sxs-lookup"><span data-stu-id="12fc3-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="12fc3-115">Esse comando remove uma solução de análise de log de monitor por pipeline.</span><span class="sxs-lookup"><span data-stu-id="12fc3-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="12fc3-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12fc3-116">PARAMETERS</span></span>

### <span data-ttu-id="12fc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fc3-117">-DefaultProfile</span></span>
<span data-ttu-id="12fc3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12fc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12fc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12fc3-119">-InputObject</span></span>
<span data-ttu-id="12fc3-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="12fc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fc3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="12fc3-121">-Name</span></span>
<span data-ttu-id="12fc3-122">Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="12fc3-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fc3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12fc3-123">-PassThru</span></span>
<span data-ttu-id="12fc3-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="12fc3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12fc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="12fc3-126">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="12fc3-126">The name of the resource group to get.</span></span>
<span data-ttu-id="12fc3-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12fc3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="12fc3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12fc3-128">-SubscriptionId</span></span>
<span data-ttu-id="12fc3-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12fc3-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12fc3-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12fc3-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12fc3-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="12fc3-131">-Confirm</span></span>
<span data-ttu-id="12fc3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12fc3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fc3-133">-WhatIf</span></span>
<span data-ttu-id="12fc3-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="12fc3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fc3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12fc3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12fc3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fc3-136">CommonParameters</span></span>
<span data-ttu-id="12fc3-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fc3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fc3-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12fc3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fc3-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="12fc3-139">INPUTS</span></span>

### <span data-ttu-id="12fc3-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="12fc3-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="12fc3-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="12fc3-141">OUTPUTS</span></span>

### <span data-ttu-id="12fc3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12fc3-142">System.Boolean</span></span>

## <span data-ttu-id="12fc3-143">Notas</span><span class="sxs-lookup"><span data-stu-id="12fc3-143">NOTES</span></span>

<span data-ttu-id="12fc3-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="12fc3-144">ALIASES</span></span>

<span data-ttu-id="12fc3-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="12fc3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12fc3-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="12fc3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12fc3-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12fc3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12fc3-148">INPUTOBJECT: <IMonitoringSolutionsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="12fc3-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12fc3-149">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="12fc3-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12fc3-150">`[ManagementAssociationName <String>]`: Nome daSsociação de Gerenciamento de Usuários.</span><span class="sxs-lookup"><span data-stu-id="12fc3-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="12fc3-151">`[ManagementConfigurationName <String>]`: Nome de configuração de gerenciamento de usuário.</span><span class="sxs-lookup"><span data-stu-id="12fc3-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="12fc3-152">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="12fc3-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="12fc3-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="12fc3-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="12fc3-154">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12fc3-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="12fc3-155">`[ResourceName <String>]`: nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="12fc3-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="12fc3-156">`[ResourceType <String>]`: Tipo de recurso para o recurso pai</span><span class="sxs-lookup"><span data-stu-id="12fc3-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="12fc3-157">`[SolutionName <String>]`: Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="12fc3-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="12fc3-158">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12fc3-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12fc3-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12fc3-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12fc3-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12fc3-160">RELATED LINKS</span></span>

