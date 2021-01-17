---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426994"
---
# <span data-ttu-id="c93ab-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c93ab-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="c93ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c93ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c93ab-103">Verifique se um nome de DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="c93ab-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="c93ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c93ab-104">SYNTAX</span></span>

### <span data-ttu-id="c93ab-105">CheckExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c93ab-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c93ab-106">Selecionar</span><span class="sxs-lookup"><span data-stu-id="c93ab-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c93ab-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c93ab-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c93ab-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c93ab-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c93ab-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c93ab-109">DESCRIPTION</span></span>
<span data-ttu-id="c93ab-110">Verifique se um nome de DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="c93ab-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="c93ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c93ab-111">EXAMPLES</span></span>

### <span data-ttu-id="c93ab-112">Exemplo 1: verificar o nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="c93ab-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="c93ab-113">Verifique a disponibilidade do nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="c93ab-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="c93ab-114">Exemplo 2: Verifique o nome de DigitalTwinsObject e CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="c93ab-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="c93ab-115">Obtenha um DigitalTwinsInstance e crie um objeto requset para testar a disponibilidade do nome.</span><span class="sxs-lookup"><span data-stu-id="c93ab-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="c93ab-116">OS</span><span class="sxs-lookup"><span data-stu-id="c93ab-116">PARAMETERS</span></span>

### <span data-ttu-id="c93ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93ab-117">-DefaultProfile</span></span>
<span data-ttu-id="c93ab-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c93ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c93ab-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="c93ab-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="c93ab-120">O resultado retornado de um banco de dados verificar solicitação de disponibilidade de nome.</span><span class="sxs-lookup"><span data-stu-id="c93ab-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="c93ab-121">Para construir, consulte a seção notas para propriedades DIGITALTWINSINSTANCECHECKNAME e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c93ab-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c93ab-122">-InputObject</span></span>
<span data-ttu-id="c93ab-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c93ab-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93ab-124">-Local</span><span class="sxs-lookup"><span data-stu-id="c93ab-124">-Location</span></span>
<span data-ttu-id="c93ab-125">Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c93ab-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93ab-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c93ab-126">-Name</span></span>
<span data-ttu-id="c93ab-127">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c93ab-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93ab-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c93ab-128">-SubscriptionId</span></span>
<span data-ttu-id="c93ab-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c93ab-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93ab-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c93ab-130">-Confirm</span></span>
<span data-ttu-id="c93ab-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c93ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c93ab-132">-WhatIf</span></span>
<span data-ttu-id="c93ab-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c93ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93ab-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c93ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93ab-135">CommonParameters</span></span>
<span data-ttu-id="c93ab-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93ab-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c93ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93ab-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c93ab-138">INPUTS</span></span>

### <span data-ttu-id="c93ab-139">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="c93ab-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="c93ab-140">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="c93ab-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="c93ab-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c93ab-141">OUTPUTS</span></span>

### <span data-ttu-id="c93ab-142">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="c93ab-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="c93ab-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c93ab-143">NOTES</span></span>

<span data-ttu-id="c93ab-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c93ab-144">ALIASES</span></span>

<span data-ttu-id="c93ab-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c93ab-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c93ab-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c93ab-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c93ab-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c93ab-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c93ab-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest> : o resultado retornado de um banco de dados verificar solicitação de disponibilidade de nome.</span><span class="sxs-lookup"><span data-stu-id="c93ab-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="c93ab-149">`Name <String>`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c93ab-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="c93ab-150">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c93ab-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c93ab-151">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c93ab-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="c93ab-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c93ab-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c93ab-153">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c93ab-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c93ab-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c93ab-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c93ab-155">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c93ab-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="c93ab-156">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c93ab-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c93ab-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c93ab-157">RELATED LINKS</span></span>

