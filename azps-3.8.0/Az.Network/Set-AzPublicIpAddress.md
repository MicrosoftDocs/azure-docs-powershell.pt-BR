---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943087"
---
# <span data-ttu-id="bb1a6-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="bb1a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1a6-103">Atualiza um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-103">Updates a public IP address.</span></span>

## <span data-ttu-id="bb1a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb1a6-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb1a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1a6-106">O cmdlet **set-AzPublicIpAddress** atualiza um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="bb1a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="bb1a6-108">1: alterar o método de alocação de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bb1a6-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="bb1a6-109">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bb1a6-110">Segundo comando define o método de alocação do objeto de endereço IP público como "estático".</span><span class="sxs-lookup"><span data-stu-id="bb1a6-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="bb1a6-111">Set-AzPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação para ' estático '.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="bb1a6-112">Um endereço IP público é alocado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="bb1a6-113">2: Adicionar rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bb1a6-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bb1a6-114">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bb1a6-115">Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="bb1a6-116">Set-AzPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="bb1a6-117">DomainNameLabel & FQDN são modificados como esperado.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="bb1a6-118">3: alterar o rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bb1a6-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bb1a6-119">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bb1a6-120">Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="bb1a6-121">Set-AzPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="bb1a6-122">DomainNameLabel & FQDN são modificados como esperado.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="bb1a6-123">OS</span><span class="sxs-lookup"><span data-stu-id="bb1a6-123">PARAMETERS</span></span>

### <span data-ttu-id="bb1a6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb1a6-124">-AsJob</span></span>
<span data-ttu-id="bb1a6-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bb1a6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb1a6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1a6-126">-DefaultProfile</span></span>
<span data-ttu-id="bb1a6-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb1a6-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-128">-PublicIpAddress</span></span>
<span data-ttu-id="bb1a6-129">Especifica um objeto de endereço IP público que representa o estado para o qual o endereço IP público deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="bb1a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1a6-130">CommonParameters</span></span>
<span data-ttu-id="bb1a6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1a6-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1a6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1a6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb1a6-133">INPUTS</span></span>

### <span data-ttu-id="bb1a6-134">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bb1a6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb1a6-135">OUTPUTS</span></span>

### <span data-ttu-id="bb1a6-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bb1a6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb1a6-137">NOTES</span></span>

## <span data-ttu-id="bb1a6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb1a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb1a6-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="bb1a6-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bb1a6-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb1a6-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


