---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110868"
---
# <span data-ttu-id="73299-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="73299-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="73299-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73299-102">SYNOPSIS</span></span>
<span data-ttu-id="73299-103">A operação Obter Serviço de Domínio recupera uma representação json do Serviço de Domínio.</span><span class="sxs-lookup"><span data-stu-id="73299-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="73299-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73299-104">SYNTAX</span></span>

### <span data-ttu-id="73299-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73299-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73299-106">Obter</span><span class="sxs-lookup"><span data-stu-id="73299-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73299-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73299-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="73299-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="73299-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73299-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="73299-109">DESCRIPTION</span></span>
<span data-ttu-id="73299-110">A operação Obter Serviço de Domínio recupera uma representação json do Serviço de Domínio.</span><span class="sxs-lookup"><span data-stu-id="73299-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="73299-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73299-111">EXAMPLES</span></span>

### <span data-ttu-id="73299-112">Exemplo 1: Obter Todos os ServiçosDoMinio Por padrão</span><span class="sxs-lookup"><span data-stu-id="73299-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="73299-113">Obter o All ADDomainService por padrão</span><span class="sxs-lookup"><span data-stu-id="73299-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="73299-114">Exemplo 2: Obter ADDomainService por ResourceGroup e nome</span><span class="sxs-lookup"><span data-stu-id="73299-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="73299-115">Obter Nome e ADDomainService por ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73299-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="73299-116">Exemplo 3: Obter todos os ADDomainService by ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73299-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="73299-117">Obter todos os ADDomainService by ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73299-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="73299-118">Exemplo 4: Obter ADDomainService por InputObject</span><span class="sxs-lookup"><span data-stu-id="73299-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="73299-119">Obter ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="73299-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="73299-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73299-120">PARAMETERS</span></span>

### <span data-ttu-id="73299-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73299-121">-DefaultProfile</span></span>
<span data-ttu-id="73299-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73299-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73299-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73299-123">-InputObject</span></span>
<span data-ttu-id="73299-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="73299-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73299-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="73299-125">-Name</span></span>
<span data-ttu-id="73299-126">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="73299-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73299-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73299-127">-ResourceGroupName</span></span>
<span data-ttu-id="73299-128">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="73299-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="73299-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73299-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="73299-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73299-130">-SubscriptionId</span></span>
<span data-ttu-id="73299-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73299-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="73299-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="73299-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73299-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73299-133">CommonParameters</span></span>
<span data-ttu-id="73299-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73299-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73299-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73299-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73299-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="73299-136">INPUTS</span></span>

### <span data-ttu-id="73299-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="73299-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="73299-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="73299-138">OUTPUTS</span></span>

### <span data-ttu-id="73299-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="73299-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="73299-140">Notas</span><span class="sxs-lookup"><span data-stu-id="73299-140">NOTES</span></span>

<span data-ttu-id="73299-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="73299-141">ALIASES</span></span>

<span data-ttu-id="73299-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="73299-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73299-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="73299-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73299-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73299-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73299-145">INPUTOBJECT: <IAdDomainServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="73299-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73299-146">`[DomainServiceName <String>]`: o nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="73299-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="73299-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="73299-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73299-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="73299-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="73299-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73299-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="73299-150">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73299-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="73299-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="73299-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="73299-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73299-152">RELATED LINKS</span></span>

