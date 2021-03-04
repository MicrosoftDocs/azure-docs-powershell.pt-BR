---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 38f9aef513e13b2676569d434977752f3d193062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889523"
---
# <span data-ttu-id="b04fb-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b04fb-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b04fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b04fb-103">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="b04fb-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="b04fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b04fb-104">SYNTAX</span></span>

### <span data-ttu-id="b04fb-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b04fb-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b04fb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b04fb-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b04fb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b04fb-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b04fb-108">List1</span><span class="sxs-lookup"><span data-stu-id="b04fb-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b04fb-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b04fb-109">DESCRIPTION</span></span>
<span data-ttu-id="b04fb-110">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="b04fb-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="b04fb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b04fb-111">EXAMPLES</span></span>

### <span data-ttu-id="b04fb-112">Exemplo 1: Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b04fb-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b04fb-113">Obter todos os DigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="b04fb-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="b04fb-114">Exemplo 2: Obter</span><span class="sxs-lookup"><span data-stu-id="b04fb-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b04fb-115">Obter o AzDigitalTwinsInstance especificado por ResourceName</span><span class="sxs-lookup"><span data-stu-id="b04fb-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="b04fb-116">Exemplo 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b04fb-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b04fb-117">Obter o AzDigitalTwinsInstance especificado por Object</span><span class="sxs-lookup"><span data-stu-id="b04fb-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="b04fb-118">Exemplo 4: List1</span><span class="sxs-lookup"><span data-stu-id="b04fb-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b04fb-119">Obter todos os DigitalTwinsInstance por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04fb-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="b04fb-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b04fb-120">PARAMETERS</span></span>

### <span data-ttu-id="b04fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04fb-121">-DefaultProfile</span></span>
<span data-ttu-id="b04fb-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b04fb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04fb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b04fb-123">-InputObject</span></span>
<span data-ttu-id="b04fb-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b04fb-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b04fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="b04fb-126">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b04fb-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04fb-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b04fb-127">-ResourceName</span></span>
<span data-ttu-id="b04fb-128">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b04fb-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04fb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b04fb-129">-SubscriptionId</span></span>
<span data-ttu-id="b04fb-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b04fb-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04fb-131">CommonParameters</span></span>
<span data-ttu-id="b04fb-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04fb-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b04fb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04fb-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b04fb-134">INPUTS</span></span>

### <span data-ttu-id="b04fb-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b04fb-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b04fb-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b04fb-136">OUTPUTS</span></span>

### <span data-ttu-id="b04fb-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b04fb-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b04fb-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="b04fb-138">NOTES</span></span>

<span data-ttu-id="b04fb-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b04fb-139">ALIASES</span></span>

<span data-ttu-id="b04fb-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b04fb-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b04fb-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b04fb-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b04fb-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b04fb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b04fb-143">INPUTOBJECT <IDigitalTwinsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b04fb-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b04fb-144">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="b04fb-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b04fb-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b04fb-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b04fb-146">`[Location <String>]`: Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b04fb-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b04fb-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b04fb-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b04fb-148">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b04fb-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b04fb-149">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b04fb-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b04fb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b04fb-150">RELATED LINKS</span></span>

