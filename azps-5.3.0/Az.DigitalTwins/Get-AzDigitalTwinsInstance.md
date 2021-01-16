---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428352"
---
# <span data-ttu-id="71388-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="71388-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="71388-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71388-102">SYNOPSIS</span></span>
<span data-ttu-id="71388-103">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="71388-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="71388-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71388-104">SYNTAX</span></span>

### <span data-ttu-id="71388-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="71388-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71388-106">Obter</span><span class="sxs-lookup"><span data-stu-id="71388-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71388-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71388-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="71388-108">List1</span><span class="sxs-lookup"><span data-stu-id="71388-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71388-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71388-109">DESCRIPTION</span></span>
<span data-ttu-id="71388-110">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="71388-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="71388-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71388-111">EXAMPLES</span></span>

### <span data-ttu-id="71388-112">Exemplo 1: lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="71388-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="71388-113">Obter todos os DigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="71388-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="71388-114">Exemplo 2: obter</span><span class="sxs-lookup"><span data-stu-id="71388-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="71388-115">Obter o AzDigitalTwinsInstance especificado por resourceName</span><span class="sxs-lookup"><span data-stu-id="71388-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="71388-116">Exemplo 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71388-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="71388-117">Obter o AzDigitalTwinsInstance especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="71388-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="71388-118">Exemplo 4: List1</span><span class="sxs-lookup"><span data-stu-id="71388-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="71388-119">Obtenha todos os DigitalTwinsInstance por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71388-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="71388-120">OS</span><span class="sxs-lookup"><span data-stu-id="71388-120">PARAMETERS</span></span>

### <span data-ttu-id="71388-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71388-121">-DefaultProfile</span></span>
<span data-ttu-id="71388-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71388-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71388-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71388-123">-InputObject</span></span>
<span data-ttu-id="71388-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71388-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71388-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71388-125">-ResourceGroupName</span></span>
<span data-ttu-id="71388-126">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71388-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="71388-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="71388-127">-ResourceName</span></span>
<span data-ttu-id="71388-128">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71388-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="71388-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71388-129">-SubscriptionId</span></span>
<span data-ttu-id="71388-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="71388-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="71388-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71388-131">CommonParameters</span></span>
<span data-ttu-id="71388-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71388-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71388-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71388-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71388-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71388-134">INPUTS</span></span>

### <span data-ttu-id="71388-135">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="71388-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="71388-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71388-136">OUTPUTS</span></span>

### <span data-ttu-id="71388-137">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="71388-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="71388-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71388-138">NOTES</span></span>

<span data-ttu-id="71388-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="71388-139">ALIASES</span></span>

<span data-ttu-id="71388-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="71388-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71388-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="71388-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71388-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71388-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71388-143">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="71388-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71388-144">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="71388-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="71388-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="71388-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71388-146">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71388-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="71388-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71388-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="71388-148">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71388-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="71388-149">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="71388-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="71388-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71388-150">RELATED LINKS</span></span>

