---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: d33f092bc72f480766ed81de66abbe1e001dfa42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889510"
---
# <span data-ttu-id="ca9b4-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ca9b4-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="ca9b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9b4-103">Verifique se um nome DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="ca9b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca9b4-104">SYNTAX</span></span>

### <span data-ttu-id="ca9b4-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca9b4-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca9b4-106">Verificar</span><span class="sxs-lookup"><span data-stu-id="ca9b4-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca9b4-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca9b4-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ca9b4-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ca9b4-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca9b4-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca9b4-109">DESCRIPTION</span></span>
<span data-ttu-id="ca9b4-110">Verifique se um nome DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="ca9b4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-111">EXAMPLES</span></span>

### <span data-ttu-id="ca9b4-112">Exemplo 1: Verifique o nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="ca9b4-113">Verifique a disponibilidade do nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="ca9b4-114">Exemplo 2: Verifique o nome por DigitalTwinsObject e CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="ca9b4-115">Obter Um DigitalTwinsInstance e criar um Objeto Requset para testar a disponibilidade do nome.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="ca9b4-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-116">PARAMETERS</span></span>

### <span data-ttu-id="ca9b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9b4-117">-DefaultProfile</span></span>
<span data-ttu-id="ca9b4-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca9b4-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="ca9b4-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="ca9b4-120">O resultado retornado de uma solicitação de disponibilidade de nome de verificação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="ca9b4-121">Para construir, consulte a seção NOTES para propriedades DIGITALTWINSINSTANCECHECKNAME e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca9b4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca9b4-122">-InputObject</span></span>
<span data-ttu-id="ca9b4-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca9b4-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ca9b4-124">-Location</span></span>
<span data-ttu-id="ca9b4-125">Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="ca9b4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ca9b4-126">-Name</span></span>
<span data-ttu-id="ca9b4-127">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-127">Resource name.</span></span>

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

### <span data-ttu-id="ca9b4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca9b4-128">-SubscriptionId</span></span>
<span data-ttu-id="ca9b4-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="ca9b4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca9b4-130">-Confirm</span></span>
<span data-ttu-id="ca9b4-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9b4-132">-WhatIf</span></span>
<span data-ttu-id="ca9b4-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9b4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9b4-135">CommonParameters</span></span>
<span data-ttu-id="ca9b4-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9b4-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca9b4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9b4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-138">INPUTS</span></span>

### <span data-ttu-id="ca9b4-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="ca9b4-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="ca9b4-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="ca9b4-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="ca9b4-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-141">OUTPUTS</span></span>

### <span data-ttu-id="ca9b4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ca9b4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="ca9b4-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca9b4-143">NOTES</span></span>

<span data-ttu-id="ca9b4-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ca9b4-144">ALIASES</span></span>

<span data-ttu-id="ca9b4-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ca9b4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca9b4-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca9b4-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca9b4-148">DIGITALTWINSINSTANCECHECKNAME : o resultado retornado de uma solicitação de disponibilidade de nome de verificação <ICheckNameRequest> de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="ca9b4-149">`Name <String>`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="ca9b4-150">INPUTOBJECT <IDigitalTwinsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ca9b4-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca9b4-151">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="ca9b4-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ca9b4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca9b4-153">`[Location <String>]`: Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ca9b4-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ca9b4-155">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="ca9b4-156">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ca9b4-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="ca9b4-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca9b4-157">RELATED LINKS</span></span>

