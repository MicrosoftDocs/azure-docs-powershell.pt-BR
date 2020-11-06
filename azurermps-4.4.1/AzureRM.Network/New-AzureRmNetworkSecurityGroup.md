---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602702"
---
# <span data-ttu-id="5e82a-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e82a-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="5e82a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e82a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e82a-103">Cria um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="5e82a-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e82a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e82a-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e82a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e82a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e82a-106">O cmdlet **New-AzureRmNetworkSecurityGroup** cria um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e82a-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="5e82a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e82a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e82a-108">1: criar um novo grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="5e82a-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="5e82a-109">Esse comando cria um novo grupo de segurança de rede do Azure chamado "nsg1" no grupo de recursos "Rg1" no local "oesteus".</span><span class="sxs-lookup"><span data-stu-id="5e82a-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="5e82a-110">2: criar um grupo de segurança de rede detalhado</span><span class="sxs-lookup"><span data-stu-id="5e82a-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="5e82a-111">Etapa: 1 Crie uma regra de segurança para permitir o acesso da Internet à porta 3389.</span><span class="sxs-lookup"><span data-stu-id="5e82a-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="5e82a-112">Etapa: 2 crie uma regra de segurança que permita o acesso da Internet à porta 80.</span><span class="sxs-lookup"><span data-stu-id="5e82a-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="5e82a-113">Etapa: 3 Adicione as regras criadas acima a um novo NSG chamado NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="5e82a-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="5e82a-114">OS</span><span class="sxs-lookup"><span data-stu-id="5e82a-114">PARAMETERS</span></span>

### <span data-ttu-id="5e82a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e82a-115">-Force</span></span>
<span data-ttu-id="5e82a-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e82a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e82a-117">-Local</span><span class="sxs-lookup"><span data-stu-id="5e82a-117">-Location</span></span>
<span data-ttu-id="5e82a-118">Especifica a região para a qual criar um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="5e82a-118">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="5e82a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e82a-119">-Name</span></span>
<span data-ttu-id="5e82a-120">Especifica o nome do grupo de segurança de rede a ser criado.</span><span class="sxs-lookup"><span data-stu-id="5e82a-120">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="5e82a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e82a-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e82a-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e82a-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5e82a-123">Esse cmdlet cria um grupo de segurança de rede no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5e82a-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e82a-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="5e82a-124">-SecurityRules</span></span>
<span data-ttu-id="5e82a-125">Especifica uma lista de objetos de regra de segurança de rede para criar em um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="5e82a-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e82a-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="5e82a-126">-Tag</span></span>
<span data-ttu-id="5e82a-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5e82a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e82a-128">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5e82a-128">For example:</span></span>

<span data-ttu-id="5e82a-129">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5e82a-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5e82a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e82a-130">-Confirm</span></span>
<span data-ttu-id="5e82a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e82a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e82a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e82a-132">-WhatIf</span></span>
<span data-ttu-id="5e82a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e82a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e82a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e82a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e82a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e82a-135">-DefaultProfile</span></span>
<span data-ttu-id="5e82a-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e82a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e82a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e82a-137">CommonParameters</span></span>
<span data-ttu-id="5e82a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e82a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e82a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e82a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e82a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e82a-140">INPUTS</span></span>

## <span data-ttu-id="5e82a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e82a-141">OUTPUTS</span></span>

### <span data-ttu-id="5e82a-142">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e82a-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5e82a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e82a-143">NOTES</span></span>

## <span data-ttu-id="5e82a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e82a-144">RELATED LINKS</span></span>

[<span data-ttu-id="5e82a-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e82a-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="5e82a-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e82a-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="5e82a-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e82a-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
