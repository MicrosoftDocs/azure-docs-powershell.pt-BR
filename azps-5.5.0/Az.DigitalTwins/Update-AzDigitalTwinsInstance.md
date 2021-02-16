---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126987"
---
# <span data-ttu-id="e0d2d-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e0d2d-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e0d2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d2d-103">Atualizar metadados do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e0d2d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0d2d-104">SYNTAX</span></span>

### <span data-ttu-id="e0d2d-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0d2d-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0d2d-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="e0d2d-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0d2d-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0d2d-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0d2d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e0d2d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0d2d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0d2d-109">DESCRIPTION</span></span>
<span data-ttu-id="e0d2d-110">Atualizar metadados do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="e0d2d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0d2d-111">EXAMPLES</span></span>

### <span data-ttu-id="e0d2d-112">Exemplo 1: UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0d2d-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e0d2d-113">Atualizar a DigitalTwinsInstance especificada por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d2d-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="e0d2d-114">Exemplo 2: Atualizar o AzDigitalTwinsInstance por outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e0d2d-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="e0d2d-115">Atualizar o AzDigitalTwinsInstance por outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="e0d2d-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="e0d2d-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0d2d-116">PARAMETERS</span></span>

### <span data-ttu-id="e0d2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d2d-117">-DefaultProfile</span></span>
<span data-ttu-id="e0d2d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0d2d-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="e0d2d-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="e0d2d-120">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="e0d2d-121">Para construir, confira a seção ANOTAÇÕES para propriedades DIGITALTWINSPATCHDESCRIPTION e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0d2d-122">-InputObject</span></span>
<span data-ttu-id="e0d2d-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0d2d-125">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e0d2d-126">-ResourceName</span></span>
<span data-ttu-id="e0d2d-127">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0d2d-128">-SubscriptionId</span></span>
<span data-ttu-id="e0d2d-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0d2d-130">-Tag</span></span>
<span data-ttu-id="e0d2d-131">Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="e0d2d-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0d2d-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0d2d-132">-Confirm</span></span>
<span data-ttu-id="e0d2d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d2d-134">-WhatIf</span></span>
<span data-ttu-id="e0d2d-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d2d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d2d-137">CommonParameters</span></span>
<span data-ttu-id="e0d2d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d2d-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0d2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d2d-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0d2d-140">INPUTS</span></span>

### <span data-ttu-id="e0d2d-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="e0d2d-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="e0d2d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="e0d2d-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="e0d2d-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0d2d-143">OUTPUTS</span></span>

### <span data-ttu-id="e0d2d-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="e0d2d-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="e0d2d-145">Notas</span><span class="sxs-lookup"><span data-stu-id="e0d2d-145">NOTES</span></span>

<span data-ttu-id="e0d2d-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="e0d2d-146">ALIASES</span></span>

<span data-ttu-id="e0d2d-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="e0d2d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0d2d-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0d2d-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0d2d-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> a descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="e0d2d-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="e0d2d-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="e0d2d-152">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="e0d2d-153">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="e0d2d-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0d2d-154">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="e0d2d-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="e0d2d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0d2d-156">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e0d2d-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e0d2d-158">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="e0d2d-159">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0d2d-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="e0d2d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0d2d-160">RELATED LINKS</span></span>

