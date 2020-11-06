---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611154"
---
# <span data-ttu-id="906cd-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="906cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="906cd-102">SYNOPSIS</span></span>
<span data-ttu-id="906cd-103">Define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="906cd-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="906cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="906cd-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="906cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="906cd-105">DESCRIPTION</span></span>
<span data-ttu-id="906cd-106">O cmdlet **set-AzureRmPublicIpAddress** define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="906cd-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="906cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="906cd-107">EXAMPLES</span></span>

### <span data-ttu-id="906cd-108">1: alterar o método de alocação de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="906cd-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="906cd-109">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="906cd-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="906cd-110">Segundo comando define o método de alocação do objeto de endereço IP público como "estático".</span><span class="sxs-lookup"><span data-stu-id="906cd-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="906cd-111">Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação para ' estático '.</span><span class="sxs-lookup"><span data-stu-id="906cd-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="906cd-112">Um endereço IP público é alocado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="906cd-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="906cd-113">2: alterar o rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="906cd-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="906cd-114">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="906cd-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="906cd-115">Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.</span><span class="sxs-lookup"><span data-stu-id="906cd-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="906cd-116">Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="906cd-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="906cd-117">DomainNameLabel & FQDN são modificados como esperado.</span><span class="sxs-lookup"><span data-stu-id="906cd-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="906cd-118">OS</span><span class="sxs-lookup"><span data-stu-id="906cd-118">PARAMETERS</span></span>

### <span data-ttu-id="906cd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="906cd-119">-AsJob</span></span>
<span data-ttu-id="906cd-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="906cd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="906cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906cd-121">-DefaultProfile</span></span>
<span data-ttu-id="906cd-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="906cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="906cd-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-123">-PublicIpAddress</span></span>
<span data-ttu-id="906cd-124">Especifica um objeto **PublicIpAddress** que representa o estado da meta para o qual o endereço IP público deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="906cd-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="906cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906cd-125">CommonParameters</span></span>
<span data-ttu-id="906cd-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906cd-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="906cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906cd-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="906cd-128">INPUTS</span></span>

### <span data-ttu-id="906cd-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-129">PSPublicIpAddress</span></span>
<span data-ttu-id="906cd-130">O parâmetro ' PublicIpAddress ' aceita o valor do tipo ' PSPublicIpAddress ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="906cd-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="906cd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="906cd-131">OUTPUTS</span></span>

### <span data-ttu-id="906cd-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="906cd-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="906cd-133">NOTES</span></span>

## <span data-ttu-id="906cd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="906cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="906cd-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="906cd-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="906cd-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="906cd-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


