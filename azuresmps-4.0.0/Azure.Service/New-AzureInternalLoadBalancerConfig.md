---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945914"
---
# <span data-ttu-id="ff763-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="ff763-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="ff763-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff763-102">SYNOPSIS</span></span>
<span data-ttu-id="ff763-103">Cria uma configuração interna de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff763-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="ff763-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff763-104">SYNTAX</span></span>

### <span data-ttu-id="ff763-105">ServiceAndSlot (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff763-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff763-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="ff763-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff763-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="ff763-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff763-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff763-108">DESCRIPTION</span></span>
<span data-ttu-id="ff763-109">O cmdlet **New-AzureInternalLoadBalancerConfig** cria um objeto **InternalLoadBalancerConfig** .</span><span class="sxs-lookup"><span data-stu-id="ff763-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="ff763-110">Você pode usar uma configuração interna de balanceador de carga ao criar uma implantação de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff763-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="ff763-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff763-111">EXAMPLES</span></span>

### <span data-ttu-id="ff763-112">Exemplo 1: criar uma configuração interna de balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="ff763-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="ff763-113">Esse comando cria uma configuração interna de balanceador de carga para a sub-rede chamada FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="ff763-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="ff763-114">O comando armazena a configuração na variável $IlbConfig para que você use para uma implantação de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff763-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="ff763-115">OS</span><span class="sxs-lookup"><span data-stu-id="ff763-115">PARAMETERS</span></span>

### <span data-ttu-id="ff763-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ff763-116">-InformationAction</span></span>
<span data-ttu-id="ff763-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ff763-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff763-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ff763-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff763-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ff763-119">Continue</span></span>
- <span data-ttu-id="ff763-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ff763-120">Ignore</span></span>
- <span data-ttu-id="ff763-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff763-121">Inquire</span></span>
- <span data-ttu-id="ff763-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff763-122">SilentlyContinue</span></span>
- <span data-ttu-id="ff763-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ff763-123">Stop</span></span>
- <span data-ttu-id="ff763-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ff763-124">Suspend</span></span>

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

### <span data-ttu-id="ff763-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff763-125">-InformationVariable</span></span>
<span data-ttu-id="ff763-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ff763-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff763-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="ff763-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="ff763-128">Especifica o nome do balanceador de carga interno que este cmdlet inclui na configuração.</span><span class="sxs-lookup"><span data-stu-id="ff763-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="ff763-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ff763-129">-Profile</span></span>
<span data-ttu-id="ff763-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ff763-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff763-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ff763-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff763-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="ff763-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="ff763-133">Especifica o endereço IP de rede virtual para um balanceador de carga interno que este cmdlet inclui na configuração.</span><span class="sxs-lookup"><span data-stu-id="ff763-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff763-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ff763-134">-SubnetName</span></span>
<span data-ttu-id="ff763-135">Especifica o nome da sub-rede para um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="ff763-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff763-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff763-136">CommonParameters</span></span>
<span data-ttu-id="ff763-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff763-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff763-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff763-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff763-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff763-139">INPUTS</span></span>

## <span data-ttu-id="ff763-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff763-140">OUTPUTS</span></span>

### <span data-ttu-id="ff763-141">Microsoft. WindowsAzure. Commands. onmanagement. Model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="ff763-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="ff763-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff763-142">NOTES</span></span>

## <span data-ttu-id="ff763-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff763-143">RELATED LINKS</span></span>

[<span data-ttu-id="ff763-144">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff763-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="ff763-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff763-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="ff763-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff763-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="ff763-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff763-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


