---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890372"
---
# <span data-ttu-id="7b70e-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="7b70e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b70e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b70e-103">Atualiza um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="7b70e-103">Updates a public IP address.</span></span>

## <span data-ttu-id="7b70e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b70e-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b70e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b70e-105">DESCRIPTION</span></span>
<span data-ttu-id="7b70e-106">O cmdlet **Set-AzPublicIpAddress** atualiza um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="7b70e-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="7b70e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b70e-107">EXAMPLES</span></span>

### <span data-ttu-id="7b70e-108">1: Alterar o método de alocação de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="7b70e-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="7b70e-109">O primeiro comando obtém o recurso de endereço IP público com $publicIPName nome no grupo de recursos $rgName.</span><span class="sxs-lookup"><span data-stu-id="7b70e-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7b70e-110">O segundo comando define o método de alocação do objeto de endereço IP público como "Static".</span><span class="sxs-lookup"><span data-stu-id="7b70e-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="7b70e-111">Set-AzPublicIPAddress o comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação como 'Static'.</span><span class="sxs-lookup"><span data-stu-id="7b70e-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="7b70e-112">Um endereço IP público é alocado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="7b70e-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="7b70e-113">2: Adicionar rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="7b70e-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="7b70e-114">O primeiro comando obtém o recurso de endereço IP público com $publicIPName nome no grupo de recursos $rgName.</span><span class="sxs-lookup"><span data-stu-id="7b70e-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7b70e-115">O segundo comando define a propriedade DomainNameLabel como o prefixo dns necessário.</span><span class="sxs-lookup"><span data-stu-id="7b70e-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="7b70e-116">Set-AzPublicIPAddress o comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="7b70e-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="7b70e-117">DomainNameLabel & Fqdn são modificados conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="7b70e-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="7b70e-118">3: Alterar o rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="7b70e-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="7b70e-119">O primeiro comando obtém o recurso de endereço IP público com $publicIPName nome no grupo de recursos $rgName.</span><span class="sxs-lookup"><span data-stu-id="7b70e-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="7b70e-120">O segundo comando define a propriedade DomainNameLabel como o prefixo dns necessário.</span><span class="sxs-lookup"><span data-stu-id="7b70e-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="7b70e-121">Set-AzPublicIPAddress o comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="7b70e-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="7b70e-122">DomainNameLabel & Fqdn são modificados conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="7b70e-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="7b70e-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b70e-123">PARAMETERS</span></span>

### <span data-ttu-id="7b70e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b70e-124">-AsJob</span></span>
<span data-ttu-id="7b70e-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7b70e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b70e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b70e-126">-DefaultProfile</span></span>
<span data-ttu-id="7b70e-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7b70e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b70e-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-128">-PublicIpAddress</span></span>
<span data-ttu-id="7b70e-129">Especifica um objeto de endereço IP público que representa o estado ao qual o endereço IP público deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="7b70e-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b70e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b70e-130">CommonParameters</span></span>
<span data-ttu-id="7b70e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b70e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b70e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b70e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b70e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b70e-133">INPUTS</span></span>

### <span data-ttu-id="7b70e-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7b70e-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b70e-135">OUTPUTS</span></span>

### <span data-ttu-id="7b70e-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7b70e-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b70e-137">NOTES</span></span>

## <span data-ttu-id="7b70e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b70e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b70e-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="7b70e-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7b70e-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b70e-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


