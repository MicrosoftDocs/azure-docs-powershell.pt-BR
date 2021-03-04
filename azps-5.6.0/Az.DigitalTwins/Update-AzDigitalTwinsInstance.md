---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 967b50b024e02d4a88fa2a1d91905acad5385b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889506"
---
# <span data-ttu-id="5eb96-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5eb96-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5eb96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb96-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb96-103">Atualizar metadados de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5eb96-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5eb96-104">SYNTAX</span></span>

### <span data-ttu-id="5eb96-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb96-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5eb96-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="5eb96-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5eb96-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5eb96-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5eb96-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5eb96-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5eb96-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5eb96-109">DESCRIPTION</span></span>
<span data-ttu-id="5eb96-110">Atualizar metadados de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="5eb96-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eb96-111">EXAMPLES</span></span>

### <span data-ttu-id="5eb96-112">Exemplo 1: UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb96-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5eb96-113">Atualizar o DigitalTwinsInstance especificado por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb96-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="5eb96-114">Exemplo 2: atualizar o AzDigitalTwinsInstance por outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5eb96-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="5eb96-115">Atualizar o AzDigitalTwinsInstance por outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="5eb96-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="5eb96-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5eb96-116">PARAMETERS</span></span>

### <span data-ttu-id="5eb96-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb96-117">-DefaultProfile</span></span>
<span data-ttu-id="5eb96-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb96-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb96-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="5eb96-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="5eb96-120">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="5eb96-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="5eb96-121">Para construir, consulte a seção NOTES para propriedades DIGITALTWINSPATCHDESCRIPTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5eb96-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="5eb96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb96-122">-InputObject</span></span>
<span data-ttu-id="5eb96-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5eb96-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5eb96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb96-124">-ResourceGroupName</span></span>
<span data-ttu-id="5eb96-125">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5eb96-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5eb96-126">-ResourceName</span></span>
<span data-ttu-id="5eb96-127">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="5eb96-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5eb96-128">-SubscriptionId</span></span>
<span data-ttu-id="5eb96-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb96-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="5eb96-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eb96-130">-Tag</span></span>
<span data-ttu-id="5eb96-131">Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="5eb96-131">Instance tags</span></span>

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

### <span data-ttu-id="5eb96-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5eb96-132">-Confirm</span></span>
<span data-ttu-id="5eb96-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb96-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb96-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb96-134">-WhatIf</span></span>
<span data-ttu-id="5eb96-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5eb96-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb96-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5eb96-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb96-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb96-137">CommonParameters</span></span>
<span data-ttu-id="5eb96-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb96-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb96-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eb96-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb96-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb96-140">INPUTS</span></span>

### <span data-ttu-id="5eb96-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="5eb96-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="5eb96-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="5eb96-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="5eb96-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5eb96-143">OUTPUTS</span></span>

### <span data-ttu-id="5eb96-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="5eb96-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="5eb96-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5eb96-145">NOTES</span></span>

<span data-ttu-id="5eb96-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5eb96-146">ALIASES</span></span>

<span data-ttu-id="5eb96-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="5eb96-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5eb96-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5eb96-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5eb96-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5eb96-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5eb96-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="5eb96-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="5eb96-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="5eb96-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="5eb96-152">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5eb96-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="5eb96-153">INPUTOBJECT <IDigitalTwinsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="5eb96-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5eb96-154">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="5eb96-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="5eb96-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5eb96-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5eb96-156">`[Location <String>]`: Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5eb96-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5eb96-158">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="5eb96-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="5eb96-159">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb96-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="5eb96-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb96-160">RELATED LINKS</span></span>

