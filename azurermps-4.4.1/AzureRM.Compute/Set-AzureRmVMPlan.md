---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: 9fc5da6afd281f68329274ae62a67d888aa13260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441386"
---
# <span data-ttu-id="34c54-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="34c54-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="34c54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34c54-102">SYNOPSIS</span></span>
<span data-ttu-id="34c54-103">Define as informações do plano do Marketplace em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34c54-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34c54-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34c54-105">DESCRIPTION</span></span>
<span data-ttu-id="34c54-106">O cmdlet **set-AzureRmVMPlan** define as informações de plano do Azure Marketplace para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34c54-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="34c54-107">Antes de poder implantar uma imagem do Marketplace por meio da linha de comando, o acesso programático deve ser habilitado ou a máquina virtual deve ser implantada usando o portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="34c54-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="34c54-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34c54-108">EXAMPLES</span></span>

## <span data-ttu-id="34c54-109">OS</span><span class="sxs-lookup"><span data-stu-id="34c54-109">PARAMETERS</span></span>

### <span data-ttu-id="34c54-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c54-110">-DefaultProfile</span></span>
<span data-ttu-id="34c54-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34c54-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c54-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="34c54-112">-Name</span></span>
<span data-ttu-id="34c54-113">Especifica o nome da imagem do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="34c54-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="34c54-114">Esse é o mesmo valor retornado pelo cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="34c54-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="34c54-115">Para obter mais informações sobre como localizar informações sobre a imagem, consulte navegando e selecionando as imagens da máquina virtual do Azure com o PowerShell e a CLI do Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) na documentação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34c54-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c54-116">-Produto</span><span class="sxs-lookup"><span data-stu-id="34c54-116">-Product</span></span>
<span data-ttu-id="34c54-117">Especifica o produto da imagem do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="34c54-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="34c54-118">Essas são as mesmas informações do valor **offer** do elemento **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="34c54-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c54-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="34c54-119">-PromotionCode</span></span>
<span data-ttu-id="34c54-120">Especifica um código promocional.</span><span class="sxs-lookup"><span data-stu-id="34c54-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c54-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="34c54-121">-Publisher</span></span>
<span data-ttu-id="34c54-122">Especifica o fornecedor da imagem.</span><span class="sxs-lookup"><span data-stu-id="34c54-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="34c54-123">Você pode encontrar essas informações usando o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="34c54-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c54-124">-VM</span><span class="sxs-lookup"><span data-stu-id="34c54-124">-VM</span></span>
<span data-ttu-id="34c54-125">Especifica o objeto da máquina virtual para o qual definir um plano do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="34c54-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="34c54-126">Você pode usar o cmdlet Get-AzureRmVM para obter um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34c54-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="34c54-127">Você pode usar o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34c54-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c54-128">CommonParameters</span></span>
<span data-ttu-id="34c54-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c54-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c54-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c54-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34c54-131">INPUTS</span></span>

## <span data-ttu-id="34c54-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34c54-132">OUTPUTS</span></span>

## <span data-ttu-id="34c54-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34c54-133">NOTES</span></span>

## <span data-ttu-id="34c54-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34c54-134">RELATED LINKS</span></span>

[<span data-ttu-id="34c54-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34c54-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="34c54-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="34c54-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="34c54-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="34c54-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="34c54-138">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="34c54-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
