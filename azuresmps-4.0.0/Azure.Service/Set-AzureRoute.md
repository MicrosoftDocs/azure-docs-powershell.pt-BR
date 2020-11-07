---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945823"
---
# <span data-ttu-id="1a20b-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="1a20b-101">Set-AzureRoute</span></span>

## <span data-ttu-id="1a20b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a20b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a20b-103">Cria uma rota em uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="1a20b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a20b-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a20b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a20b-105">DESCRIPTION</span></span>
<span data-ttu-id="1a20b-106">O cmdlet **set-AzureRoute** cria uma rota em uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="1a20b-107">A nova rota entra praticamente em vigor praticamente nas máquinas virtuais associadas à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="1a20b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a20b-108">EXAMPLES</span></span>

### <span data-ttu-id="1a20b-109">Exemplo 1: adicionar um dispositivo virtual próximo caminho de salto</span><span class="sxs-lookup"><span data-stu-id="1a20b-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="1a20b-110">Esse comando cria uma tabela de rota chamada ApplianceRouteTable no local especificado.</span><span class="sxs-lookup"><span data-stu-id="1a20b-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="1a20b-111">O comando transmite essa tabela de rota para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1a20b-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="1a20b-112">O cmdlet Current adiciona uma rota chamada ApplianceRoute03, que é um tipo de salto do VirtualAppliance próximo.</span><span class="sxs-lookup"><span data-stu-id="1a20b-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="1a20b-113">O comando especifica o próximo endereço IP do salto e o prefixo do endereço para a rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="1a20b-114">Exemplo 2: adicionar uma rota da Internet no próximo salto</span><span class="sxs-lookup"><span data-stu-id="1a20b-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="1a20b-115">Esse comando obtém uma tabela de rota chamada ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="1a20b-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="1a20b-116">O comando transmite essa tabela de rota para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1a20b-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="1a20b-117">O cmdlet atual adiciona uma rota chamada InternetRoute, que é um tipo de salto seguinte na Internet.</span><span class="sxs-lookup"><span data-stu-id="1a20b-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="1a20b-118">O comando especifica o prefixo do endereço para a rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="1a20b-119">OS</span><span class="sxs-lookup"><span data-stu-id="1a20b-119">PARAMETERS</span></span>

### <span data-ttu-id="1a20b-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1a20b-120">-AddressPrefix</span></span>
<span data-ttu-id="1a20b-121">Especifica um prefixo de endereço para a nova rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-121">Specifies an address prefix for the new route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1a20b-122">-NextHopIpAddress</span></span>
<span data-ttu-id="1a20b-123">Especifica o endereço IP do dispositivo que é o próximo nó do tráfego que usa essa rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="1a20b-124">Especifique esse valor apenas se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="1a20b-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="1a20b-125">-NextHopType</span></span>
<span data-ttu-id="1a20b-126">Especifica o próximo tipo de salto para tráfego que usa essa rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="1a20b-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1a20b-127">Valid values are:</span></span> 

- <span data-ttu-id="1a20b-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="1a20b-128">VPNGateway</span></span>
- <span data-ttu-id="1a20b-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="1a20b-129">VNETLocal</span></span>
- <span data-ttu-id="1a20b-130">Rede</span><span class="sxs-lookup"><span data-stu-id="1a20b-130">Internet</span></span>
- <span data-ttu-id="1a20b-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1a20b-131">VirtualAppliance</span></span>
- <span data-ttu-id="1a20b-132">Vazio</span><span class="sxs-lookup"><span data-stu-id="1a20b-132">Null</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1a20b-133">-Profile</span></span>
<span data-ttu-id="1a20b-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1a20b-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1a20b-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1a20b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1a20b-136">-RouteName</span></span>
<span data-ttu-id="1a20b-137">Especifica um nome para a nova rota que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="1a20b-137">Specifies a name for the new route that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1a20b-138">-RouteTable</span></span>
<span data-ttu-id="1a20b-139">Especifica a tabela de rota para a qual esse cmdlet adiciona a nova rota.</span><span class="sxs-lookup"><span data-stu-id="1a20b-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a20b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a20b-140">CommonParameters</span></span>
<span data-ttu-id="1a20b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a20b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a20b-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a20b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a20b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a20b-143">INPUTS</span></span>

## <span data-ttu-id="1a20b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a20b-144">OUTPUTS</span></span>

## <span data-ttu-id="1a20b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a20b-145">NOTES</span></span>

## <span data-ttu-id="1a20b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a20b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1a20b-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="1a20b-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


