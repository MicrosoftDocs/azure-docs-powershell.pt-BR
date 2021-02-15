---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6299fcc8828031b61aabc912fcd30c1ed8cbb0e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113845"
---
# <span data-ttu-id="57ab1-101">Get-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="57ab1-101">Get-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="57ab1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="57ab1-103">Obter o Ponto de Extremidade DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="57ab1-103">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="57ab1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57ab1-104">SYNTAX</span></span>

### <span data-ttu-id="57ab1-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57ab1-105">List (Default)</span></span>
```
Get-AzDigitalTwinsEndpoint -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57ab1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="57ab1-106">Get</span></span>
```
Get-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57ab1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57ab1-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="57ab1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="57ab1-109">Obter o Ponto de Extremidade DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="57ab1-109">Get DigitalTwinsInstances Endpoint.</span></span>

## <span data-ttu-id="57ab1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="57ab1-111">Exemplo 1: Lista AzDigitalTwinsEndpoint no ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57ab1-111">Example 1: List AzDigitalTwinsEndpoint in ResourceGroup</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57ab1-112">Listar todos os AzDigitalTwinsEndpoints por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ab1-112">List all AzDigitalTwinsEndpoints by ResourceGroupName</span></span>

### <span data-ttu-id="57ab1-113">Exemplo 2: Obter o AzDigitalTwinsEndpoint por EndpointName</span><span class="sxs-lookup"><span data-stu-id="57ab1-113">Example 2: Get AzDigitalTwinsEndpoint by EndpointName</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57ab1-114">Obter o AzDigitalTwinsEndpoint por EndpointName no ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57ab1-114">Get AzDigitalTwinsEndpoint by EndpointName in ResourceGroup</span></span>

### <span data-ttu-id="57ab1-115">Exemplo 3: Obter o AzDigitalTwinsEndpoint por objeto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="57ab1-115">Example 3: Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>
```powershell
PS C:\> $GetAzDigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriDigitalTwinEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Get-AzDigitalTwinsEndpoint -InputObject $GetAzDigitalTwinsEndpoint

Name                     Type
----                     ----
youriDigitalTwinEndpoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="57ab1-116">Obter o AzDigitalTwinsEndpoint por Objeto 'AzDigitalTwinsEndpoint'</span><span class="sxs-lookup"><span data-stu-id="57ab1-116">Get AzDigitalTwinsEndpoint by 'AzDigitalTwinsEndpoint' Object</span></span>

## <span data-ttu-id="57ab1-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57ab1-117">PARAMETERS</span></span>

### <span data-ttu-id="57ab1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ab1-118">-DefaultProfile</span></span>
<span data-ttu-id="57ab1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57ab1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ab1-120">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="57ab1-120">-EndpointName</span></span>
<span data-ttu-id="57ab1-121">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="57ab1-121">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="57ab1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ab1-122">-InputObject</span></span>
<span data-ttu-id="57ab1-123">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="57ab1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57ab1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ab1-124">-ResourceGroupName</span></span>
<span data-ttu-id="57ab1-125">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="57ab1-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="57ab1-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="57ab1-126">-ResourceName</span></span>
<span data-ttu-id="57ab1-127">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="57ab1-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="57ab1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57ab1-128">-SubscriptionId</span></span>
<span data-ttu-id="57ab1-129">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="57ab1-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="57ab1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ab1-130">CommonParameters</span></span>
<span data-ttu-id="57ab1-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ab1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ab1-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ab1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ab1-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="57ab1-133">INPUTS</span></span>

### <span data-ttu-id="57ab1-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="57ab1-134">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="57ab1-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="57ab1-135">OUTPUTS</span></span>

### <span data-ttu-id="57ab1-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="57ab1-136">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="57ab1-137">Notas</span><span class="sxs-lookup"><span data-stu-id="57ab1-137">NOTES</span></span>

<span data-ttu-id="57ab1-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="57ab1-138">ALIASES</span></span>

<span data-ttu-id="57ab1-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="57ab1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57ab1-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="57ab1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57ab1-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57ab1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57ab1-142">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="57ab1-142">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57ab1-143">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="57ab1-143">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="57ab1-144">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="57ab1-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57ab1-145">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="57ab1-145">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="57ab1-146">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="57ab1-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="57ab1-147">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="57ab1-147">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="57ab1-148">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="57ab1-148">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="57ab1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57ab1-149">RELATED LINKS</span></span>

