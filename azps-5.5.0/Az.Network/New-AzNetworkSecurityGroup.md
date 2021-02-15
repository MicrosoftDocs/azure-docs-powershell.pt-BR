---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117388"
---
# <span data-ttu-id="9f6fe-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f6fe-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="9f6fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6fe-103">Cria um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-103">Creates a network security group.</span></span>

## <span data-ttu-id="9f6fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f6fe-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6fe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f6fe-105">DESCRIPTION</span></span>
<span data-ttu-id="9f6fe-106">O **cmdlet New-AzNetworkSecurityGroup** cria um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="9f6fe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f6fe-107">EXAMPLES</span></span>

### <span data-ttu-id="9f6fe-108">Exemplo 1: Criar um novo grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="9f6fe-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="9f6fe-109">Esse comando cria um novo grupo de segurança de rede do Azure chamado "nsg1" no grupo de recursos "rg1" no local "westus".</span><span class="sxs-lookup"><span data-stu-id="9f6fe-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="9f6fe-110">Exemplo 2: Criar um grupo de segurança de rede detalhado</span><span class="sxs-lookup"><span data-stu-id="9f6fe-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="9f6fe-111">Etapa:1 Criar uma regra de segurança que permita o acesso da Internet à porta 3389.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="9f6fe-112">Etapa:2 Criar uma regra de segurança que permita o acesso da Internet à porta 80.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="9f6fe-113">Etapa:3 Adicione as regras criadas acima a um novo NSG chamado NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="9f6fe-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f6fe-114">PARAMETERS</span></span>

### <span data-ttu-id="9f6fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f6fe-115">-AsJob</span></span>
<span data-ttu-id="9f6fe-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f6fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f6fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6fe-117">-DefaultProfile</span></span>
<span data-ttu-id="9f6fe-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f6fe-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9f6fe-119">-Force</span></span>
<span data-ttu-id="9f6fe-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f6fe-121">-Local</span><span class="sxs-lookup"><span data-stu-id="9f6fe-121">-Location</span></span>
<span data-ttu-id="9f6fe-122">Especifica a região para a qual criar um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="9f6fe-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f6fe-123">-Name</span></span>
<span data-ttu-id="9f6fe-124">Especifica o nome do grupo de segurança de rede a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="9f6fe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6fe-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f6fe-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9f6fe-127">Esse cmdlet cria um grupo de segurança de rede no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f6fe-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="9f6fe-128">-SecurityRules</span></span>
<span data-ttu-id="9f6fe-129">Especifica uma lista de objetos de regra de segurança de rede para criar em um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6fe-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f6fe-130">-Tag</span></span>
<span data-ttu-id="9f6fe-131">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9f6fe-132">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9f6fe-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9f6fe-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f6fe-133">-Confirm</span></span>
<span data-ttu-id="9f6fe-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6fe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6fe-135">-WhatIf</span></span>
<span data-ttu-id="9f6fe-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6fe-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6fe-138">CommonParameters</span></span>
<span data-ttu-id="9f6fe-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6fe-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6fe-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6fe-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f6fe-141">INPUTS</span></span>

### <span data-ttu-id="9f6fe-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9f6fe-142">System.String</span></span>

### <span data-ttu-id="9f6fe-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="9f6fe-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="9f6fe-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9f6fe-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9f6fe-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f6fe-145">OUTPUTS</span></span>

### <span data-ttu-id="9f6fe-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f6fe-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9f6fe-147">Notas</span><span class="sxs-lookup"><span data-stu-id="9f6fe-147">NOTES</span></span>

## <span data-ttu-id="9f6fe-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f6fe-148">RELATED LINKS</span></span>

[<span data-ttu-id="9f6fe-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f6fe-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9f6fe-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f6fe-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9f6fe-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f6fe-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
