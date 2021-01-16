---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429575"
---
# <span data-ttu-id="2da8d-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2da8d-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="2da8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2da8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2da8d-103">Cria um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="2da8d-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="2da8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2da8d-104">SYNTAX</span></span>

### <span data-ttu-id="2da8d-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2da8d-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da8d-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="2da8d-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2da8d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2da8d-107">DESCRIPTION</span></span>
<span data-ttu-id="2da8d-108">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="2da8d-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="2da8d-109">O cmdlet **New-AzLocalNetworkGateway** cria o objeto que representa o gateway local de acordo com o nome, o nome do grupo de recursos, o local e o endereço IP do gateway, bem como o prefixo do endereço da rede local que será conectada ao Azure.</span><span class="sxs-lookup"><span data-stu-id="2da8d-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="2da8d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2da8d-110">EXAMPLES</span></span>

### <span data-ttu-id="2da8d-111">Exemplo 1: criar um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="2da8d-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="2da8d-112">Cria o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" no local "West US" com o endereço IP "23.99.221.164" e o prefixo de endereço "10.5.51.0/24" local.</span><span class="sxs-lookup"><span data-stu-id="2da8d-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="2da8d-113">OS</span><span class="sxs-lookup"><span data-stu-id="2da8d-113">PARAMETERS</span></span>

### <span data-ttu-id="2da8d-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2da8d-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="2da8d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2da8d-115">-AsJob</span></span>
<span data-ttu-id="2da8d-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2da8d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2da8d-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="2da8d-117">-Asn</span></span>
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

### <span data-ttu-id="2da8d-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2da8d-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="2da8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da8d-119">-DefaultProfile</span></span>
<span data-ttu-id="2da8d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2da8d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da8d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2da8d-121">-Force</span></span>
<span data-ttu-id="2da8d-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2da8d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2da8d-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2da8d-123">-Fqdn</span></span>
<span data-ttu-id="2da8d-124">FQDN do gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="2da8d-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da8d-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2da8d-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da8d-126">-Local</span><span class="sxs-lookup"><span data-stu-id="2da8d-126">-Location</span></span>
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

### <span data-ttu-id="2da8d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2da8d-127">-Name</span></span>
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

### <span data-ttu-id="2da8d-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2da8d-128">-PeerWeight</span></span>
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

### <span data-ttu-id="2da8d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da8d-129">-ResourceGroupName</span></span>
<span data-ttu-id="2da8d-130">Especifica o grupo de recursos ao qual pertence o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="2da8d-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="2da8d-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="2da8d-131">-Tag</span></span>
<span data-ttu-id="2da8d-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2da8d-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2da8d-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2da8d-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2da8d-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2da8d-134">-Confirm</span></span>
<span data-ttu-id="2da8d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da8d-136">-WhatIf</span></span>
<span data-ttu-id="2da8d-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2da8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2da8d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2da8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da8d-139">CommonParameters</span></span>
<span data-ttu-id="2da8d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da8d-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2da8d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da8d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2da8d-142">INPUTS</span></span>

### <span data-ttu-id="2da8d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2da8d-143">System.String</span></span>

### <span data-ttu-id="2da8d-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="2da8d-144">System.String[]</span></span>

### <span data-ttu-id="2da8d-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2da8d-145">System.UInt32</span></span>

### <span data-ttu-id="2da8d-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2da8d-146">System.Int32</span></span>

### <span data-ttu-id="2da8d-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2da8d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2da8d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2da8d-148">OUTPUTS</span></span>

### <span data-ttu-id="2da8d-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2da8d-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="2da8d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2da8d-150">NOTES</span></span>

## <span data-ttu-id="2da8d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2da8d-151">RELATED LINKS</span></span>

[<span data-ttu-id="2da8d-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2da8d-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="2da8d-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2da8d-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="2da8d-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2da8d-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
