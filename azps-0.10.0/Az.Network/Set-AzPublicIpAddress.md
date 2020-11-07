---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776516"
---
# <span data-ttu-id="2700a-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="2700a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2700a-102">SYNOPSIS</span></span>
<span data-ttu-id="2700a-103">Define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2700a-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="2700a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2700a-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2700a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2700a-105">DESCRIPTION</span></span>
<span data-ttu-id="2700a-106">O cmdlet **set-AzPublicIpAddress** define o estado da meta para um endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="2700a-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="2700a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2700a-107">EXAMPLES</span></span>

### <span data-ttu-id="2700a-108">1: alterar o método de alocação de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="2700a-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="2700a-109">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2700a-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="2700a-110">Segundo comando define o método de alocação do objeto de endereço IP público como "estático".</span><span class="sxs-lookup"><span data-stu-id="2700a-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="2700a-111">Set-AzPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação para ' estático '.</span><span class="sxs-lookup"><span data-stu-id="2700a-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="2700a-112">Um endereço IP público é alocado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="2700a-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="2700a-113">2: alterar o rótulo de domínio DNS de um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="2700a-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="2700a-114">Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2700a-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="2700a-115">Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2700a-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="2700a-116">Set-AzPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado.</span><span class="sxs-lookup"><span data-stu-id="2700a-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="2700a-117">DomainNameLabel & FQDN são modificados como esperado.</span><span class="sxs-lookup"><span data-stu-id="2700a-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="2700a-118">OS</span><span class="sxs-lookup"><span data-stu-id="2700a-118">PARAMETERS</span></span>

### <span data-ttu-id="2700a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2700a-119">-AsJob</span></span>
<span data-ttu-id="2700a-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2700a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2700a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2700a-121">-DefaultProfile</span></span>
<span data-ttu-id="2700a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2700a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2700a-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-123">-PublicIpAddress</span></span>
<span data-ttu-id="2700a-124">Especifica um objeto **PublicIpAddress** que representa o estado da meta para o qual o endereço IP público deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="2700a-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="2700a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2700a-125">CommonParameters</span></span>
<span data-ttu-id="2700a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2700a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2700a-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2700a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2700a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2700a-128">INPUTS</span></span>

### <span data-ttu-id="2700a-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-129">PSPublicIpAddress</span></span>
<span data-ttu-id="2700a-130">O parâmetro ' PublicIpAddress ' aceita o valor do tipo ' PSPublicIpAddress ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2700a-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="2700a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2700a-131">OUTPUTS</span></span>

### <span data-ttu-id="2700a-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2700a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2700a-133">NOTES</span></span>

## <span data-ttu-id="2700a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2700a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2700a-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="2700a-136">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="2700a-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2700a-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


