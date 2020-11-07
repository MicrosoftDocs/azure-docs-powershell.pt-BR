---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945724"
---
# <span data-ttu-id="1b1c3-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b1c3-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="1b1c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1c3-103">Adiciona um balanceador de carga interno a um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="1b1c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b1c3-104">SYNTAX</span></span>

### <span data-ttu-id="1b1c3-105">ServiceAndSlot (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b1c3-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b1c3-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="1b1c3-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1b1c3-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="1b1c3-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1b1c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b1c3-108">DESCRIPTION</span></span>
<span data-ttu-id="1b1c3-109">O cmdlet **Add-AzureInternalLoadBalancer** adiciona uma configuração interna de balanceador de carga a um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="1b1c3-110">Para uma rede virtual, você pode especificar uma sub-rede ou o endereço IP do balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="1b1c3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b1c3-111">EXAMPLES</span></span>

### <span data-ttu-id="1b1c3-112">Exemplo 1: adicionar um balanceador de carga interno</span><span class="sxs-lookup"><span data-stu-id="1b1c3-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="1b1c3-113">Esse comando adiciona um balanceador de carga interno chamado ContosoILB ao serviço chamado ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="1b1c3-114">Exemplo 2: adicionar um balanceador de carga interno para uma sub-rede especificada</span><span class="sxs-lookup"><span data-stu-id="1b1c3-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="1b1c3-115">Esse comando adiciona um balanceador de carga interno chamado ContosoILB ao serviço chamado ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="1b1c3-116">O comando especifica a sub-rede chamada FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="1b1c3-117">Exemplo 3: adicionar um balanceador de carga interno para um endereço e uma sub-rede especificada</span><span class="sxs-lookup"><span data-stu-id="1b1c3-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="1b1c3-118">Esse comando adiciona um balanceador de carga interno chamado ContosoILB ao serviço chamado ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="1b1c3-119">O comando especifica a sub-rede chamada FrontEndSubnet e o endereço estático da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="1b1c3-120">OS</span><span class="sxs-lookup"><span data-stu-id="1b1c3-120">PARAMETERS</span></span>

### <span data-ttu-id="1b1c3-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1b1c3-121">-InformationAction</span></span>
<span data-ttu-id="1b1c3-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1b1c3-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1b1c3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b1c3-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="1b1c3-124">Continue</span></span>
- <span data-ttu-id="1b1c3-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="1b1c3-125">Ignore</span></span>
- <span data-ttu-id="1b1c3-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="1b1c3-126">Inquire</span></span>
- <span data-ttu-id="1b1c3-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1b1c3-127">SilentlyContinue</span></span>
- <span data-ttu-id="1b1c3-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="1b1c3-128">Stop</span></span>
- <span data-ttu-id="1b1c3-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="1b1c3-129">Suspend</span></span>

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

### <span data-ttu-id="1b1c3-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1b1c3-130">-InformationVariable</span></span>
<span data-ttu-id="1b1c3-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1b1c3-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="1b1c3-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="1b1c3-133">Especifica o nome do balanceador de carga interno que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1b1c3-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1b1c3-134">-Profile</span></span>
<span data-ttu-id="1b1c3-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b1c3-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b1c3-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1b1c3-137">-ServiceName</span></span>
<span data-ttu-id="1b1c3-138">Especifica o nome do serviço para o qual esse cmdlet adiciona um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="1b1c3-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="1b1c3-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="1b1c3-140">Especifica o endereço IP de rede virtual para um balanceador de carga interno que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1b1c3-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1b1c3-141">-SubnetName</span></span>
<span data-ttu-id="1b1c3-142">Especifica o nome da sub-rede para um balanceador de carga interno que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1b1c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1c3-143">CommonParameters</span></span>
<span data-ttu-id="1b1c3-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1c3-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1c3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1c3-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b1c3-146">INPUTS</span></span>

## <span data-ttu-id="1b1c3-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b1c3-147">OUTPUTS</span></span>

### <span data-ttu-id="1b1c3-148">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="1b1c3-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="1b1c3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b1c3-149">NOTES</span></span>

## <span data-ttu-id="1b1c3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b1c3-150">RELATED LINKS</span></span>

[<span data-ttu-id="1b1c3-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b1c3-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="1b1c3-152">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="1b1c3-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="1b1c3-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b1c3-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="1b1c3-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b1c3-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


