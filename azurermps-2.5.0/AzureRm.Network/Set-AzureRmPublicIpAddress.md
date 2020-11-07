---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: d78e4d8e84508e9a737bb15dc31b0dad1c9bdedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785637"
---
# <span data-ttu-id="d3548-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d3548-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3548-102">SYNOPSIS</span></span>
<span data-ttu-id="d3548-103">Define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="d3548-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3548-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3548-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3548-105">DESCRIPTION</span></span>
<span data-ttu-id="d3548-106">O cmdlet **set-AzureRmPublicIpAddress** define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="d3548-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="d3548-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3548-107">EXAMPLES</span></span>

### <span data-ttu-id="d3548-108">1: alterar o método de alocação de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="d3548-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="d3548-109">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3548-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d3548-110">Segundo comando define o método de alocação do objeto de endereço IP público como "estático".</span><span class="sxs-lookup"><span data-stu-id="d3548-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="d3548-111">Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação para ' estático '.</span><span class="sxs-lookup"><span data-stu-id="d3548-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="d3548-112">Um endereço IP público é alocado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d3548-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="d3548-113">2: alterar o rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="d3548-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d3548-114">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3548-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d3548-115">Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d3548-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="d3548-116">Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="d3548-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="d3548-117">DomainNameLabel & FQDN são modificados como esperado.</span><span class="sxs-lookup"><span data-stu-id="d3548-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="d3548-118">OS</span><span class="sxs-lookup"><span data-stu-id="d3548-118">PARAMETERS</span></span>

### <span data-ttu-id="d3548-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3548-119">-AsJob</span></span>
<span data-ttu-id="d3548-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d3548-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3548-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3548-121">-DefaultProfile</span></span>
<span data-ttu-id="d3548-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3548-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3548-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-123">-PublicIpAddress</span></span>
<span data-ttu-id="d3548-124">Especifica um objeto **PublicIpAddress** que representa o estado da meta para o qual o endereço IP público deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="d3548-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3548-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3548-125">CommonParameters</span></span>
<span data-ttu-id="d3548-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3548-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3548-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3548-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3548-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3548-128">INPUTS</span></span>

### <span data-ttu-id="d3548-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-129">PSPublicIpAddress</span></span>
<span data-ttu-id="d3548-130">O parâmetro ' PublicIpAddress ' aceita o valor do tipo ' PSPublicIpAddress ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d3548-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="d3548-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3548-131">OUTPUTS</span></span>

### <span data-ttu-id="d3548-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d3548-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3548-133">NOTES</span></span>

## <span data-ttu-id="d3548-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3548-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3548-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d3548-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d3548-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3548-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


