---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 35ba036e38b54a335cbdcdd923008a5a4ce055fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889525"
---
# <span data-ttu-id="90ed8-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="90ed8-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="90ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="90ed8-103">Obter Ponto de Extremidade DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="90ed8-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="90ed8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90ed8-104">SYNTAX</span></span>

### <span data-ttu-id="90ed8-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90ed8-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90ed8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="90ed8-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90ed8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90ed8-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="90ed8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="90ed8-109">Obter Ponto de Extremidade DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="90ed8-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="90ed8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90ed8-110">EXAMPLES</span></span>

### <span data-ttu-id="90ed8-111">Exemplo 1: Listar AzDigitalTwinsEndpoint em ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90ed8-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="90ed8-112">Listar todos os AzDigitalTwinsEndpoints por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ed8-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="90ed8-113">Exemplo 2: Obter AzDigitalTwinsEndpoint por EndpointName</span><span class="sxs-lookup"><span data-stu-id="90ed8-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="90ed8-114">Obter AzDigitalTwinsEndpoint por EndpointName em ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90ed8-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="90ed8-115">Exemplo 3: Obter o objeto AzDigitalTwinsEndpoint por 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="90ed8-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="90ed8-116">Obter o objeto AzDigitalTwinsEndpoint por 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="90ed8-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="90ed8-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90ed8-117">PARAMETERS</span></span>

### <span data-ttu-id="90ed8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ed8-118">-DefaultProfile</span></span>
<span data-ttu-id="90ed8-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90ed8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ed8-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="90ed8-120">-EndpointName</span></span>
<span data-ttu-id="90ed8-121">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="90ed8-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="90ed8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ed8-122">-InputObject</span></span>
<span data-ttu-id="90ed8-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="90ed8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90ed8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ed8-124">-ResourceGroupName</span></span>
<span data-ttu-id="90ed8-125">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="90ed8-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="90ed8-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="90ed8-126">-ResourceName</span></span>
<span data-ttu-id="90ed8-127">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="90ed8-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="90ed8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90ed8-128">-SubscriptionId</span></span>
<span data-ttu-id="90ed8-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="90ed8-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="90ed8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ed8-130">CommonParameters</span></span>
<span data-ttu-id="90ed8-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ed8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ed8-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ed8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ed8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90ed8-133">INPUTS</span></span>

### <span data-ttu-id="90ed8-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="90ed8-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="90ed8-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90ed8-135">OUTPUTS</span></span>

### <span data-ttu-id="90ed8-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="90ed8-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="90ed8-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="90ed8-137">NOTES</span></span>

<span data-ttu-id="90ed8-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90ed8-138">ALIASES</span></span>

<span data-ttu-id="90ed8-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="90ed8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90ed8-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="90ed8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90ed8-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90ed8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90ed8-142">INPUTOBJECT <IDigitalTwinsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="90ed8-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90ed8-143">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="90ed8-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="90ed8-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="90ed8-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90ed8-145">`[Location <String>]`: Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="90ed8-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="90ed8-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="90ed8-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="90ed8-147">`[ResourceName <String>]`: O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="90ed8-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="90ed8-148">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="90ed8-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="90ed8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90ed8-149">RELATED LINKS</span></span>

