---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117675"
---
# <span data-ttu-id="9f415-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="9f415-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="9f415-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f415-102">SYNOPSIS</span></span>
<span data-ttu-id="9f415-103">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="9f415-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="9f415-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f415-104">SYNTAX</span></span>

### <span data-ttu-id="9f415-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f415-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9f415-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9f415-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9f415-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f415-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f415-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="9f415-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9f415-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f415-109">DESCRIPTION</span></span>
<span data-ttu-id="9f415-110">Obter o recurso DigitalTwinsInstances.</span><span class="sxs-lookup"><span data-stu-id="9f415-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="9f415-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f415-111">EXAMPLES</span></span>

### <span data-ttu-id="9f415-112">Exemplo 1: Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f415-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="9f415-113">Obter toda a DigitalTwinsInstance por padrão</span><span class="sxs-lookup"><span data-stu-id="9f415-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="9f415-114">Exemplo 2: Obter</span><span class="sxs-lookup"><span data-stu-id="9f415-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="9f415-115">Obter o AzDigitalTwinsInstance especificado por ResourceName</span><span class="sxs-lookup"><span data-stu-id="9f415-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="9f415-116">Exemplo 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f415-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="9f415-117">Obter o AzDigitalTwinsInstance especificado por Objeto</span><span class="sxs-lookup"><span data-stu-id="9f415-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="9f415-118">Exemplo 4: Lista1</span><span class="sxs-lookup"><span data-stu-id="9f415-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="9f415-119">Obter toda a DigitalTwinsInstance por ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f415-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="9f415-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f415-120">PARAMETERS</span></span>

### <span data-ttu-id="9f415-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f415-121">-DefaultProfile</span></span>
<span data-ttu-id="9f415-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f415-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f415-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f415-123">-InputObject</span></span>
<span data-ttu-id="9f415-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9f415-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f415-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f415-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f415-126">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="9f415-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="9f415-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9f415-127">-ResourceName</span></span>
<span data-ttu-id="9f415-128">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="9f415-128">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="9f415-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f415-129">-SubscriptionId</span></span>
<span data-ttu-id="9f415-130">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f415-130">The subscription identifier.</span></span>

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

### <span data-ttu-id="9f415-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f415-131">CommonParameters</span></span>
<span data-ttu-id="9f415-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f415-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f415-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f415-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f415-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f415-134">INPUTS</span></span>

### <span data-ttu-id="9f415-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="9f415-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="9f415-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f415-136">OUTPUTS</span></span>

### <span data-ttu-id="9f415-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="9f415-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="9f415-138">Notas</span><span class="sxs-lookup"><span data-stu-id="9f415-138">NOTES</span></span>

<span data-ttu-id="9f415-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="9f415-139">ALIASES</span></span>

<span data-ttu-id="9f415-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="9f415-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f415-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9f415-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f415-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f415-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f415-143">INPUTOBJECT: <IDigitalTwinsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="9f415-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f415-144">`[EndpointName <String>]`: Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="9f415-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="9f415-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="9f415-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f415-146">`[Location <String>]`: Localização do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="9f415-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="9f415-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="9f415-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="9f415-148">`[ResourceName <String>]`: o nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="9f415-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="9f415-149">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f415-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="9f415-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f415-150">RELATED LINKS</span></span>

