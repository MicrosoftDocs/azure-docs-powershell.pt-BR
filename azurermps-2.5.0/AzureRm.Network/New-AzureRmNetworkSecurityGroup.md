---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 3603adcce2ce39cc4e0a2dd57869a6ca10c48998
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785905"
---
# <span data-ttu-id="215f7-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215f7-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="215f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="215f7-102">SYNOPSIS</span></span>
<span data-ttu-id="215f7-103">Cria um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="215f7-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="215f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="215f7-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="215f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="215f7-105">DESCRIPTION</span></span>
<span data-ttu-id="215f7-106">O cmdlet **New-AzureRmNetworkSecurityGroup** cria um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="215f7-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="215f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="215f7-107">EXAMPLES</span></span>

### <span data-ttu-id="215f7-108">1: criar um novo grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="215f7-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="215f7-109">Esse comando cria um novo grupo de segurança de rede do Azure chamado "nsg1" no grupo de recursos "Rg1" no local "oesteus".</span><span class="sxs-lookup"><span data-stu-id="215f7-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="215f7-110">2: criar um grupo de segurança de rede detalhado</span><span class="sxs-lookup"><span data-stu-id="215f7-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="215f7-111">Etapa: 1 Crie uma regra de segurança para permitir o acesso da Internet à porta 3389.</span><span class="sxs-lookup"><span data-stu-id="215f7-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="215f7-112">Etapa: 2 crie uma regra de segurança que permita o acesso da Internet à porta 80.</span><span class="sxs-lookup"><span data-stu-id="215f7-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="215f7-113">Etapa: 3 Adicione as regras criadas acima a um novo NSG chamado NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="215f7-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="215f7-114">OS</span><span class="sxs-lookup"><span data-stu-id="215f7-114">PARAMETERS</span></span>

### <span data-ttu-id="215f7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="215f7-115">-AsJob</span></span>
<span data-ttu-id="215f7-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="215f7-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215f7-117">-DefaultProfile</span></span>
<span data-ttu-id="215f7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="215f7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="215f7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="215f7-119">-Force</span></span>
<span data-ttu-id="215f7-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="215f7-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-121">-Local</span><span class="sxs-lookup"><span data-stu-id="215f7-121">-Location</span></span>
<span data-ttu-id="215f7-122">Especifica a região para a qual criar um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="215f7-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="215f7-123">-Name</span></span>
<span data-ttu-id="215f7-124">Especifica o nome do grupo de segurança de rede a ser criado.</span><span class="sxs-lookup"><span data-stu-id="215f7-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="215f7-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="215f7-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="215f7-127">Esse cmdlet cria um grupo de segurança de rede no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="215f7-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="215f7-128">-SecurityRules</span></span>
<span data-ttu-id="215f7-129">Especifica uma lista de objetos de regra de segurança de rede para criar em um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="215f7-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="215f7-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="215f7-130">-Tag</span></span>
<span data-ttu-id="215f7-131">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="215f7-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="215f7-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="215f7-132">For example:</span></span>

<span data-ttu-id="215f7-133">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="215f7-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="215f7-134">-Confirm</span></span>
<span data-ttu-id="215f7-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="215f7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="215f7-136">-WhatIf</span></span>
<span data-ttu-id="215f7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="215f7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="215f7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="215f7-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215f7-139">CommonParameters</span></span>
<span data-ttu-id="215f7-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="215f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215f7-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215f7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215f7-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="215f7-142">INPUTS</span></span>

## <span data-ttu-id="215f7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="215f7-143">OUTPUTS</span></span>

### <span data-ttu-id="215f7-144">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215f7-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="215f7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="215f7-145">NOTES</span></span>

## <span data-ttu-id="215f7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="215f7-146">RELATED LINKS</span></span>

[<span data-ttu-id="215f7-147">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215f7-147">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="215f7-148">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215f7-148">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="215f7-149">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="215f7-149">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
