---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945954"
---
# <span data-ttu-id="948e3-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="948e3-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="948e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="948e3-102">SYNOPSIS</span></span>
<span data-ttu-id="948e3-103">Modifica uma configuração interna de balanceador de carga em um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="948e3-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="948e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="948e3-104">SYNTAX</span></span>

### <span data-ttu-id="948e3-105">ServiceAndSlot (padrão)</span><span class="sxs-lookup"><span data-stu-id="948e3-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="948e3-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="948e3-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="948e3-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="948e3-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="948e3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="948e3-108">DESCRIPTION</span></span>
<span data-ttu-id="948e3-109">O cmdlet **set-AzureInternalLoadBalancer** modifica uma configuração interna de balanceador de carga em um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="948e3-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="948e3-110">Para uma rede virtual, você pode especificar uma sub-rede ou o endereço IP do balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="948e3-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="948e3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="948e3-111">EXAMPLES</span></span>

### <span data-ttu-id="948e3-112">1:</span><span class="sxs-lookup"><span data-stu-id="948e3-112">1:</span></span>
```

```

## <span data-ttu-id="948e3-113">OS</span><span class="sxs-lookup"><span data-stu-id="948e3-113">PARAMETERS</span></span>

### <span data-ttu-id="948e3-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="948e3-114">-InformationAction</span></span>
<span data-ttu-id="948e3-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="948e3-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="948e3-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="948e3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="948e3-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="948e3-117">Continue</span></span>
- <span data-ttu-id="948e3-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="948e3-118">Ignore</span></span>
- <span data-ttu-id="948e3-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="948e3-119">Inquire</span></span>
- <span data-ttu-id="948e3-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="948e3-120">SilentlyContinue</span></span>
- <span data-ttu-id="948e3-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="948e3-121">Stop</span></span>
- <span data-ttu-id="948e3-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="948e3-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="948e3-123">-InformationVariable</span></span>
<span data-ttu-id="948e3-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="948e3-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="948e3-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="948e3-126">Especifica o nome do balanceador de carga interno que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="948e3-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="948e3-127">-Profile</span></span>
<span data-ttu-id="948e3-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="948e3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="948e3-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="948e3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="948e3-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="948e3-130">-ServiceName</span></span>
<span data-ttu-id="948e3-131">Especifica o nome do serviço em que esse cmdlet modifica um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="948e3-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="948e3-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="948e3-133">Especifica o endereço IP de rede virtual para um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="948e3-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="948e3-134">-SubnetName</span></span>
<span data-ttu-id="948e3-135">Especifica o nome da sub-rede para um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="948e3-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948e3-136">CommonParameters</span></span>
<span data-ttu-id="948e3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="948e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948e3-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948e3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948e3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="948e3-139">INPUTS</span></span>

## <span data-ttu-id="948e3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="948e3-140">OUTPUTS</span></span>

## <span data-ttu-id="948e3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="948e3-141">NOTES</span></span>

## <span data-ttu-id="948e3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="948e3-142">RELATED LINKS</span></span>

[<span data-ttu-id="948e3-143">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="948e3-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="948e3-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="948e3-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="948e3-145">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="948e3-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="948e3-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="948e3-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


