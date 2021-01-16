---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260531"
---
# <span data-ttu-id="21078-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="21078-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="21078-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21078-102">SYNOPSIS</span></span>
<span data-ttu-id="21078-103">Atualize os metadados de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="21078-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21078-104">SYNTAX</span></span>

### <span data-ttu-id="21078-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="21078-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="21078-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="21078-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="21078-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21078-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="21078-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="21078-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="21078-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21078-109">DESCRIPTION</span></span>
<span data-ttu-id="21078-110">Atualize os metadados de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="21078-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21078-111">EXAMPLES</span></span>

### <span data-ttu-id="21078-112">Exemplo 1: UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="21078-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="21078-113">Atualizar o DigitalTwinsInstance especificado por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21078-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="21078-114">Exemplo 2: atualizar a AzDigitalTwinsInstance de outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="21078-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="21078-115">Atualizar o AzDigitalTwinsInstance por outro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="21078-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="21078-116">OS</span><span class="sxs-lookup"><span data-stu-id="21078-116">PARAMETERS</span></span>

### <span data-ttu-id="21078-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21078-117">-DefaultProfile</span></span>
<span data-ttu-id="21078-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21078-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21078-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="21078-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="21078-120">A descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="21078-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="21078-121">Para construir, consulte a seção notas para propriedades DIGITALTWINSPATCHDESCRIPTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="21078-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="21078-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21078-122">-InputObject</span></span>
<span data-ttu-id="21078-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="21078-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21078-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21078-124">-ResourceGroupName</span></span>
<span data-ttu-id="21078-125">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="21078-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="21078-126">-ResourceName</span></span>
<span data-ttu-id="21078-127">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="21078-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21078-128">-SubscriptionId</span></span>
<span data-ttu-id="21078-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="21078-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="21078-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="21078-130">-Tag</span></span>
<span data-ttu-id="21078-131">Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="21078-131">Instance tags</span></span>

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

### <span data-ttu-id="21078-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21078-132">-Confirm</span></span>
<span data-ttu-id="21078-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21078-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21078-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21078-134">-WhatIf</span></span>
<span data-ttu-id="21078-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21078-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21078-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21078-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21078-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21078-137">CommonParameters</span></span>
<span data-ttu-id="21078-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21078-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21078-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21078-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21078-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21078-140">INPUTS</span></span>

### <span data-ttu-id="21078-141">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="21078-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="21078-142">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="21078-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="21078-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21078-143">OUTPUTS</span></span>

### <span data-ttu-id="21078-144">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="21078-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="21078-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21078-145">NOTES</span></span>

<span data-ttu-id="21078-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="21078-146">ALIASES</span></span>

<span data-ttu-id="21078-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="21078-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21078-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="21078-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21078-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="21078-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21078-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : a descrição do serviço DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="21078-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="21078-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Marcas de instância</span><span class="sxs-lookup"><span data-stu-id="21078-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="21078-152">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="21078-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="21078-153">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="21078-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21078-154">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="21078-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="21078-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="21078-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21078-156">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21078-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21078-158">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="21078-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="21078-159">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="21078-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="21078-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21078-160">RELATED LINKS</span></span>

