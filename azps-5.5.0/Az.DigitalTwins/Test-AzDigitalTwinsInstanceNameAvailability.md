---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117674"
---
# <span data-ttu-id="16c37-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="16c37-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="16c37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16c37-102">SYNOPSIS</span></span>
<span data-ttu-id="16c37-103">Verifique se um nome DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="16c37-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="16c37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16c37-104">SYNTAX</span></span>

### <span data-ttu-id="16c37-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="16c37-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16c37-106">Verificar</span><span class="sxs-lookup"><span data-stu-id="16c37-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16c37-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16c37-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="16c37-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16c37-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16c37-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="16c37-109">DESCRIPTION</span></span>
<span data-ttu-id="16c37-110">Verifique se um nome DigitalTwinsInstance está disponível.</span><span class="sxs-lookup"><span data-stu-id="16c37-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="16c37-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16c37-111">EXAMPLES</span></span>

### <span data-ttu-id="16c37-112">Exemplo 1: Verificar o nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="16c37-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="16c37-113">Verifique a disponibilidade do nome por local e nome.</span><span class="sxs-lookup"><span data-stu-id="16c37-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="16c37-114">Exemplo 2: Verifique o nome por DigitalTwinsObject e CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="16c37-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="16c37-115">Obter um DigitalTwinsInstance e criar um Objeto Requset para testar a disponibilidade do nome.</span><span class="sxs-lookup"><span data-stu-id="16c37-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="16c37-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16c37-116">PARAMETERS</span></span>

### <span data-ttu-id="16c37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c37-117">-DefaultProfile</span></span>
<span data-ttu-id="16c37-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16c37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c37-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="16c37-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="16c37-120">O resultado retornado de uma solicitação de disponibilidade de nome de verificação de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16c37-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="16c37-121">Para construir, confira a seção ANOTAÇÕES para propriedades DIGITALTWINSINSTANCECHECKNAME e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="16c37-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c37-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c37-122">-InputObject</span></span>
<span data-ttu-id="16c37-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="16c37-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c37-124">-Local</span><span class="sxs-lookup"><span data-stu-id="16c37-124">-Location</span></span>
<span data-ttu-id="16c37-125">Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="16c37-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="16c37-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="16c37-126">-Name</span></span>
<span data-ttu-id="16c37-127">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="16c37-127">Resource name.</span></span>

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

### <span data-ttu-id="16c37-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c37-128">-SubscriptionId</span></span>
<span data-ttu-id="16c37-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="16c37-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="16c37-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16c37-130">-Confirm</span></span>
<span data-ttu-id="16c37-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c37-132">-WhatIf</span></span>
<span data-ttu-id="16c37-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16c37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c37-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16c37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c37-135">CommonParameters</span></span>
<span data-ttu-id="16c37-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c37-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16c37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c37-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="16c37-138">INPUTS</span></span>

### <span data-ttu-id="16c37-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="16c37-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="16c37-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="16c37-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="16c37-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="16c37-141">OUTPUTS</span></span>

### <span data-ttu-id="16c37-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="16c37-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="16c37-143">Notas</span><span class="sxs-lookup"><span data-stu-id="16c37-143">NOTES</span></span>

<span data-ttu-id="16c37-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="16c37-144">ALIASES</span></span>

<span data-ttu-id="16c37-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="16c37-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16c37-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="16c37-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16c37-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16c37-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16c37-148">DIGITALTWINSINSTANCECHECKNAME: o resultado retornado de uma solicitação de disponibilidade de nome de verificação <ICheckNameRequest> de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16c37-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="16c37-149">`Name <String>`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="16c37-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="16c37-150">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="16c37-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16c37-151">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="16c37-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="16c37-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="16c37-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16c37-153">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="16c37-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="16c37-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="16c37-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="16c37-155">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="16c37-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="16c37-156">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="16c37-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="16c37-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16c37-157">RELATED LINKS</span></span>

