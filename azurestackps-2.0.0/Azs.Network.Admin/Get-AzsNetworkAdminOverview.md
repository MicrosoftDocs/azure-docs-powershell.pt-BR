---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775994"
---
# <span data-ttu-id="d18af-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="d18af-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="d18af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d18af-102">SYNOPSIS</span></span>
<span data-ttu-id="d18af-103">Obtenha uma visão geral do estado do provedor de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="d18af-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="d18af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d18af-104">SYNTAX</span></span>

### <span data-ttu-id="d18af-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="d18af-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d18af-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d18af-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d18af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d18af-107">DESCRIPTION</span></span>
<span data-ttu-id="d18af-108">Obtenha uma visão geral do estado do provedor de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="d18af-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="d18af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d18af-109">EXAMPLES</span></span>

### <span data-ttu-id="d18af-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d18af-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="d18af-111">OS</span><span class="sxs-lookup"><span data-stu-id="d18af-111">PARAMETERS</span></span>

### <span data-ttu-id="d18af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18af-112">-DefaultProfile</span></span>
<span data-ttu-id="d18af-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d18af-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d18af-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d18af-114">-InputObject</span></span>
<span data-ttu-id="d18af-115">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d18af-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d18af-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d18af-116">-SubscriptionId</span></span>
<span data-ttu-id="d18af-117">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d18af-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d18af-118">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d18af-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d18af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18af-119">CommonParameters</span></span>
<span data-ttu-id="d18af-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18af-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d18af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18af-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d18af-122">INPUTS</span></span>

### <span data-ttu-id="d18af-123">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d18af-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="d18af-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d18af-124">OUTPUTS</span></span>

### <span data-ttu-id="d18af-125">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="d18af-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="d18af-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d18af-126">NOTES</span></span>

<span data-ttu-id="d18af-127">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d18af-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d18af-128">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d18af-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d18af-129">INPUTobject <INetworkAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d18af-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d18af-130">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d18af-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d18af-131">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d18af-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d18af-132">`[ResourceName <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d18af-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="d18af-133">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d18af-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d18af-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d18af-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d18af-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d18af-135">RELATED LINKS</span></span>

