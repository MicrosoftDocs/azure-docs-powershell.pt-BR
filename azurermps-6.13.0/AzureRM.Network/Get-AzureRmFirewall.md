---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610561"
---
# <span data-ttu-id="4536a-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4536a-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="4536a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4536a-102">SYNOPSIS</span></span>
<span data-ttu-id="4536a-103">Obtém um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="4536a-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4536a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4536a-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4536a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4536a-105">DESCRIPTION</span></span>
<span data-ttu-id="4536a-106">O cmdlet **Get-AzureRmFirewall** Obtém um ou mais firewalls em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4536a-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="4536a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4536a-107">EXAMPLES</span></span>

### <span data-ttu-id="4536a-108">1: recuperar todos os firewalls em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4536a-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="4536a-109">Este exemplo recupera todos os firewalls no grupo de recursos "rgName".</span><span class="sxs-lookup"><span data-stu-id="4536a-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="4536a-110">2: recuperar um firewall por nome</span><span class="sxs-lookup"><span data-stu-id="4536a-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="4536a-111">Este exemplo recupera o firewall chamado "azFw" no grupo de recursos "rgName".</span><span class="sxs-lookup"><span data-stu-id="4536a-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="4536a-112">3: recuperar um firewall e adicionar uma coleção de regras de aplicativo ao firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="4536a-113">Este exemplo recupera um firewall e, em seguida, adiciona um conjunto de regras de aplicativo ao firewall chamando o método AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="4536a-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="4536a-114">4: recuperar um firewall e adicionar uma coleção de regras de rede ao firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="4536a-115">Este exemplo recupera um firewall e, em seguida, adiciona um conjunto de regras de rede ao firewall chamando o método AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="4536a-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="4536a-116">5: recuperar um firewall e recuperar uma coleção de regras de aplicativo por nome do firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="4536a-117">Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetApplicationRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="4536a-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="4536a-118">O nome da coleção de regras para o método GetApplicationRuleCollectionByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4536a-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="4536a-119">6: recuperar um firewall e recuperar uma coleção de regras de rede por nome do firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="4536a-120">Este exemplo recupera um firewall e obtém uma coleção de regras por nome, método de chamada GetNetworkRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="4536a-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="4536a-121">O nome da coleção de regras para o método GetNetworkRuleCollectionByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4536a-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="4536a-122">7: recuperar um firewall e remover uma coleção de regras de aplicativo por nome do firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="4536a-123">Este exemplo recupera um firewall e, em seguida, remove uma coleção de regras por nome, método de chamada RemoveApplicationRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="4536a-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="4536a-124">O nome da coleção de regras para o método RemoveApplicationRuleCollectionByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4536a-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="4536a-125">8: recuperar um firewall e remover uma coleção de regras de rede por nome do firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="4536a-126">Este exemplo recupera um firewall e, em seguida, remove uma coleção de regras por nome, método de chamada RemoveNetworkRuleCollectionByName no objeto de firewall.</span><span class="sxs-lookup"><span data-stu-id="4536a-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="4536a-127">O nome da coleção de regras para o método RemoveNetworkRuleCollectionByName não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4536a-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="4536a-128">9: recuperar um firewall e depois atribuir o firewall</span><span class="sxs-lookup"><span data-stu-id="4536a-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="4536a-129">Este exemplo recupera um firewall e chama Allocate no firewall para iniciar o serviço de firewall usando a configuração (coleções de regras de aplicativo e de rede) associadas ao firewall.</span><span class="sxs-lookup"><span data-stu-id="4536a-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="4536a-130">OS</span><span class="sxs-lookup"><span data-stu-id="4536a-130">PARAMETERS</span></span>

### <span data-ttu-id="4536a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4536a-131">-DefaultProfile</span></span>
<span data-ttu-id="4536a-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4536a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4536a-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="4536a-133">-Name</span></span>
<span data-ttu-id="4536a-134">Especifica o nome do firewall que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4536a-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4536a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4536a-135">-ResourceGroupName</span></span>
<span data-ttu-id="4536a-136">Especifica o nome do grupo de recursos ao qual o firewall pertence.</span><span class="sxs-lookup"><span data-stu-id="4536a-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4536a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4536a-137">CommonParameters</span></span>
<span data-ttu-id="4536a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4536a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4536a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4536a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4536a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4536a-140">INPUTS</span></span>

### <span data-ttu-id="4536a-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4536a-141">None</span></span>
<span data-ttu-id="4536a-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4536a-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4536a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4536a-143">OUTPUTS</span></span>

### <span data-ttu-id="4536a-144">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="4536a-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="4536a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4536a-145">NOTES</span></span>

## <span data-ttu-id="4536a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4536a-146">RELATED LINKS</span></span>

[<span data-ttu-id="4536a-147">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4536a-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="4536a-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4536a-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="4536a-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4536a-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
