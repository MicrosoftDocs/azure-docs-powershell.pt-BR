---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260551"
---
# <span data-ttu-id="d2de9-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2de9-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="d2de9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2de9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2de9-103">Obtenha o DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d2de9-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="d2de9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2de9-104">SYNTAX</span></span>

### <span data-ttu-id="d2de9-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2de9-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2de9-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d2de9-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2de9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2de9-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2de9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2de9-108">DESCRIPTION</span></span>
<span data-ttu-id="d2de9-109">Obtenha o DigitalTwinsInstances Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d2de9-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="d2de9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2de9-110">EXAMPLES</span></span>

### <span data-ttu-id="d2de9-111">Exemplo 1: list AzDigitalTwinsEndpoint no MySource</span><span class="sxs-lookup"><span data-stu-id="d2de9-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d2de9-112">Liste todos os AzDigitalTwinsEndpoints por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2de9-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="d2de9-113">Exemplo 2: obter AzDigitalTwinsEndpoint por EndpointName</span><span class="sxs-lookup"><span data-stu-id="d2de9-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d2de9-114">Obter AzDigitalTwinsEndpoint por EndpointName em um MySource</span><span class="sxs-lookup"><span data-stu-id="d2de9-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="d2de9-115">Exemplo 3: obter AzDigitalTwinsEndpoint pelo objeto ' AzDigitalTwinsEndpoint '</span><span class="sxs-lookup"><span data-stu-id="d2de9-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="d2de9-116">Obter AzDigitalTwinsEndpoint pelo objeto ' AzDigitalTwinsEndpoint '</span><span class="sxs-lookup"><span data-stu-id="d2de9-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="d2de9-117">OS</span><span class="sxs-lookup"><span data-stu-id="d2de9-117">PARAMETERS</span></span>

### <span data-ttu-id="d2de9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2de9-118">-DefaultProfile</span></span>
<span data-ttu-id="d2de9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2de9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2de9-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d2de9-120">-EndpointName</span></span>
<span data-ttu-id="d2de9-121">Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d2de9-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="d2de9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2de9-122">-InputObject</span></span>
<span data-ttu-id="d2de9-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d2de9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2de9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2de9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2de9-125">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d2de9-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2de9-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d2de9-126">-ResourceName</span></span>
<span data-ttu-id="d2de9-127">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d2de9-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2de9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2de9-128">-SubscriptionId</span></span>
<span data-ttu-id="d2de9-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d2de9-129">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2de9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2de9-130">CommonParameters</span></span>
<span data-ttu-id="d2de9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2de9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2de9-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2de9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2de9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2de9-133">INPUTS</span></span>

### <span data-ttu-id="d2de9-134">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d2de9-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="d2de9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2de9-135">OUTPUTS</span></span>

### <span data-ttu-id="d2de9-136">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="d2de9-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="d2de9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2de9-137">NOTES</span></span>

<span data-ttu-id="d2de9-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2de9-138">ALIASES</span></span>

<span data-ttu-id="d2de9-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d2de9-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2de9-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d2de9-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2de9-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2de9-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2de9-142">INPUTobject <IDigitalTwinsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d2de9-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2de9-143">`[EndpointName <String>]`: Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d2de9-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="d2de9-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d2de9-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2de9-145">`[Location <String>]`: Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d2de9-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d2de9-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d2de9-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d2de9-147">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d2de9-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="d2de9-148">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d2de9-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="d2de9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2de9-149">RELATED LINKS</span></span>

