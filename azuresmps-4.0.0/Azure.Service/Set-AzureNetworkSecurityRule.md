---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945800"
---
# <span data-ttu-id="552e2-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="552e2-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="552e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="552e2-102">SYNOPSIS</span></span>
<span data-ttu-id="552e2-103">Adiciona ou modifica uma regra de segurança de rede em um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="552e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="552e2-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="552e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="552e2-105">DESCRIPTION</span></span>
<span data-ttu-id="552e2-106">O cmdlet **set-AzureNetworkSecurityRule** adiciona ou modifica uma regra de segurança de rede do Azure em um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="552e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="552e2-107">EXAMPLES</span></span>

## <span data-ttu-id="552e2-108">OS</span><span class="sxs-lookup"><span data-stu-id="552e2-108">PARAMETERS</span></span>

### <span data-ttu-id="552e2-109">-Ação</span><span class="sxs-lookup"><span data-stu-id="552e2-109">-Action</span></span>
<span data-ttu-id="552e2-110">Especifica a ação para uma regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="552e2-111">Os valores válidos são: allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="552e2-111">Valid values are: Allow and Deny.</span></span>

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

### <span data-ttu-id="552e2-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="552e2-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="552e2-113">Especifica o endereço de roteamento interdomain sem classe (CIDR) do intervalo de IP de destino para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="552e2-114">Um asterisco (\*) Especifica qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="552e2-114">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="552e2-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="552e2-115">-DestinationPortRange</span></span>
<span data-ttu-id="552e2-116">Especifica um intervalo de porta de destino para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="552e2-117">Os valores válidos consistem em números inteiros de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="552e2-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="552e2-118">Você pode especificar um valor individual ou especificar um intervalo no formato LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="552e2-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="552e2-119">Um hífen separa os dois valores.</span><span class="sxs-lookup"><span data-stu-id="552e2-119">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="552e2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="552e2-120">-Name</span></span>
<span data-ttu-id="552e2-121">Especifica o nome da regra de segurança de rede que este cmdlet adiciona ou modifica.</span><span class="sxs-lookup"><span data-stu-id="552e2-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

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

### <span data-ttu-id="552e2-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="552e2-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="552e2-123">Especifica o grupo de segurança de rede que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="552e2-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="552e2-124">Para obter um objeto **INetworkSecurityGroup** , use o cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="552e2-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="552e2-125">-Priority</span><span class="sxs-lookup"><span data-stu-id="552e2-125">-Priority</span></span>
<span data-ttu-id="552e2-126">Especifica a prioridade para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="552e2-127">Os valores válidos são: inteiros de 100 a 4096.</span><span class="sxs-lookup"><span data-stu-id="552e2-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="552e2-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="552e2-128">-Profile</span></span>
<span data-ttu-id="552e2-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="552e2-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="552e2-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="552e2-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="552e2-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="552e2-131">-Protocol</span></span>
<span data-ttu-id="552e2-132">Especifica o protocolo para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="552e2-133">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="552e2-133">Valid values are:</span></span> 

- <span data-ttu-id="552e2-134">Protocol</span><span class="sxs-lookup"><span data-stu-id="552e2-134">TCP</span></span> 
- <span data-ttu-id="552e2-135">GRAMA</span><span class="sxs-lookup"><span data-stu-id="552e2-135">UDP</span></span> 
- *

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

### <span data-ttu-id="552e2-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="552e2-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="552e2-137">Especifica o endereço CIDR do intervalo de IP de origem para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="552e2-138">Um asterisco (\*) Especifica qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="552e2-138">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="552e2-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="552e2-139">-SourcePortRange</span></span>
<span data-ttu-id="552e2-140">Especifica um intervalo de porta de origem para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="552e2-141">Os valores válidos consistem em números inteiros de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="552e2-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="552e2-142">Você pode especificar um valor individual ou especificar um intervalo no formato LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="552e2-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="552e2-143">Um hífen separa os dois valores.</span><span class="sxs-lookup"><span data-stu-id="552e2-143">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="552e2-144">-Digite</span><span class="sxs-lookup"><span data-stu-id="552e2-144">-Type</span></span>
<span data-ttu-id="552e2-145">Especifica o tipo de conexão para a regra de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="552e2-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="552e2-146">Os valores válidos são: de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="552e2-146">Valid values are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="552e2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552e2-147">CommonParameters</span></span>
<span data-ttu-id="552e2-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="552e2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552e2-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="552e2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552e2-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="552e2-150">INPUTS</span></span>

## <span data-ttu-id="552e2-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="552e2-151">OUTPUTS</span></span>

## <span data-ttu-id="552e2-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="552e2-152">NOTES</span></span>

## <span data-ttu-id="552e2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="552e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="552e2-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="552e2-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


