---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 9f622a6796cd63aeb6a4de760b21fd487d210af2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600315"
---
# <span data-ttu-id="f65ec-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f65ec-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f65ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f65ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f65ec-103">Cria um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="f65ec-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="f65ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f65ec-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f65ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f65ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f65ec-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="f65ec-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f65ec-107">O cmdlet **New-AzLocalNetworkGateway** cria o objeto que representa o gateway local de acordo com o nome, o nome do grupo de recursos, o local e o endereço IP do gateway, bem como o prefixo do endereço da rede local que será conectada ao Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ec-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="f65ec-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f65ec-108">EXAMPLES</span></span>

### <span data-ttu-id="f65ec-109">1: criar um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="f65ec-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="f65ec-110">Cria o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" no local "West US" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" local.</span><span class="sxs-lookup"><span data-stu-id="f65ec-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="f65ec-111">OS</span><span class="sxs-lookup"><span data-stu-id="f65ec-111">PARAMETERS</span></span>

### <span data-ttu-id="f65ec-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f65ec-112">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f65ec-113">-AsJob</span></span>
<span data-ttu-id="f65ec-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f65ec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f65ec-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="f65ec-115">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f65ec-116">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65ec-117">-DefaultProfile</span></span>
<span data-ttu-id="f65ec-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f65ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f65ec-119">-Force</span></span>
<span data-ttu-id="f65ec-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f65ec-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f65ec-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="f65ec-121">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-122">-Local</span><span class="sxs-lookup"><span data-stu-id="f65ec-122">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f65ec-123">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f65ec-124">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="f65ec-126">Especifica o grupo de recursos ao qual pertence o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="f65ec-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="f65ec-127">-Tag</span></span>
<span data-ttu-id="f65ec-128">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f65ec-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f65ec-129">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f65ec-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f65ec-130">-Confirm</span></span>
<span data-ttu-id="f65ec-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f65ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f65ec-132">-WhatIf</span></span>
<span data-ttu-id="f65ec-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f65ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f65ec-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f65ec-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65ec-135">CommonParameters</span></span>
<span data-ttu-id="f65ec-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65ec-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65ec-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f65ec-138">INPUTS</span></span>

### <span data-ttu-id="f65ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f65ec-139">System.String</span></span>

### <span data-ttu-id="f65ec-140">System. String []</span><span class="sxs-lookup"><span data-stu-id="f65ec-140">System.String[]</span></span>

### <span data-ttu-id="f65ec-141">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f65ec-141">System.UInt32</span></span>

### <span data-ttu-id="f65ec-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f65ec-142">System.Int32</span></span>

### <span data-ttu-id="f65ec-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f65ec-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f65ec-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f65ec-144">OUTPUTS</span></span>

### <span data-ttu-id="f65ec-145">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f65ec-145">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f65ec-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f65ec-146">NOTES</span></span>

## <span data-ttu-id="f65ec-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f65ec-147">RELATED LINKS</span></span>

[<span data-ttu-id="f65ec-148">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f65ec-148">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f65ec-149">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f65ec-149">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="f65ec-150">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f65ec-150">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
