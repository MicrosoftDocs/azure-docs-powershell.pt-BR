---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945213"
---
# <span data-ttu-id="d840a-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="d840a-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="d840a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d840a-102">SYNOPSIS</span></span>
<span data-ttu-id="d840a-103">Obter uma cota por nome.</span><span class="sxs-lookup"><span data-stu-id="d840a-103">Get a quota by name.</span></span>

## <span data-ttu-id="d840a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d840a-104">SYNTAX</span></span>

### <span data-ttu-id="d840a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d840a-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d840a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d840a-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d840a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d840a-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d840a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d840a-108">DESCRIPTION</span></span>
<span data-ttu-id="d840a-109">Listar todas as cotas.</span><span class="sxs-lookup"><span data-stu-id="d840a-109">List all quotas.</span></span>
<span data-ttu-id="d840a-110">Limite a lista passando um nome ou um filtro.</span><span class="sxs-lookup"><span data-stu-id="d840a-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="d840a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d840a-111">EXAMPLES</span></span>

### <span data-ttu-id="d840a-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d840a-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="d840a-113">Lista todas as cotas de rede.</span><span class="sxs-lookup"><span data-stu-id="d840a-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="d840a-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d840a-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="d840a-115">Obtém a cota de rede especificada.</span><span class="sxs-lookup"><span data-stu-id="d840a-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="d840a-116">OS</span><span class="sxs-lookup"><span data-stu-id="d840a-116">PARAMETERS</span></span>

### <span data-ttu-id="d840a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d840a-117">-DefaultProfile</span></span>
<span data-ttu-id="d840a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d840a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d840a-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d840a-119">-Filter</span></span>
<span data-ttu-id="d840a-120">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d840a-120">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d840a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d840a-121">-InputObject</span></span>
<span data-ttu-id="d840a-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d840a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d840a-123">-Local</span><span class="sxs-lookup"><span data-stu-id="d840a-123">-Location</span></span>
<span data-ttu-id="d840a-124">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d840a-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d840a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d840a-125">-Name</span></span>
<span data-ttu-id="d840a-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d840a-126">Name of the resource.</span></span>

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

### <span data-ttu-id="d840a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d840a-127">-PassThru</span></span>
<span data-ttu-id="d840a-128">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d840a-128">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d840a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d840a-129">-SubscriptionId</span></span>
<span data-ttu-id="d840a-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d840a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d840a-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d840a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d840a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d840a-132">CommonParameters</span></span>
<span data-ttu-id="d840a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d840a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d840a-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d840a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d840a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d840a-135">INPUTS</span></span>

### <span data-ttu-id="d840a-136">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d840a-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="d840a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d840a-137">OUTPUTS</span></span>

### <span data-ttu-id="d840a-138">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d840a-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="d840a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d840a-139">NOTES</span></span>

<span data-ttu-id="d840a-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d840a-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d840a-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d840a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d840a-142">INPUTobject <INetworkAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d840a-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d840a-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d840a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d840a-144">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d840a-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d840a-145">`[ResourceName <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d840a-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="d840a-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d840a-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d840a-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d840a-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d840a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d840a-148">RELATED LINKS</span></span>

