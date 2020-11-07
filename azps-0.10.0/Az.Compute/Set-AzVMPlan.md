---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 63c23712373cd597766faff8fd57f7f4b38deaa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776824"
---
# <span data-ttu-id="9b30b-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="9b30b-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="9b30b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b30b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b30b-103">Define as informações do plano do Marketplace em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b30b-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="9b30b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b30b-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b30b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b30b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b30b-106">O cmdlet **set-AzVMPlan** define as informações de plano do Azure Marketplace para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b30b-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="9b30b-107">Antes de poder implantar uma imagem do Marketplace por meio da linha de comando, o acesso programático deve ser habilitado ou a máquina virtual deve ser implantada usando o portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="9b30b-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="9b30b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b30b-108">EXAMPLES</span></span>

## <span data-ttu-id="9b30b-109">OS</span><span class="sxs-lookup"><span data-stu-id="9b30b-109">PARAMETERS</span></span>

### <span data-ttu-id="9b30b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b30b-110">-DefaultProfile</span></span>
<span data-ttu-id="9b30b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b30b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b30b-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b30b-112">-Name</span></span>
<span data-ttu-id="9b30b-113">Especifica o nome da imagem do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9b30b-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="9b30b-114">Esse é o mesmo valor retornado pelo cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9b30b-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="9b30b-115">Para obter mais informações sobre como localizar informações sobre a imagem, consulte navegando e selecionando as imagens da máquina virtual do Azure com o PowerShell e a CLI do Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) na documentação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b30b-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b30b-116">-Produto</span><span class="sxs-lookup"><span data-stu-id="9b30b-116">-Product</span></span>
<span data-ttu-id="9b30b-117">Especifica o produto da imagem do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9b30b-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="9b30b-118">Essas são as mesmas informações do valor **offer** do elemento **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="9b30b-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b30b-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="9b30b-119">-PromotionCode</span></span>
<span data-ttu-id="9b30b-120">Especifica um código promocional.</span><span class="sxs-lookup"><span data-stu-id="9b30b-120">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b30b-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9b30b-121">-Publisher</span></span>
<span data-ttu-id="9b30b-122">Especifica o fornecedor da imagem.</span><span class="sxs-lookup"><span data-stu-id="9b30b-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="9b30b-123">Você pode encontrar essas informações usando o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9b30b-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b30b-124">-VM</span><span class="sxs-lookup"><span data-stu-id="9b30b-124">-VM</span></span>
<span data-ttu-id="9b30b-125">Especifica o objeto da máquina virtual para o qual definir um plano do Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9b30b-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="9b30b-126">Você pode usar o cmdlet Get-AzVM para obter um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b30b-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="9b30b-127">Você pode usar o cmdlet New-AzVMConfig para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b30b-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b30b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b30b-128">CommonParameters</span></span>
<span data-ttu-id="9b30b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b30b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b30b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b30b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b30b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b30b-131">INPUTS</span></span>

### <span data-ttu-id="9b30b-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9b30b-132">PSVirtualMachine</span></span>
<span data-ttu-id="9b30b-133">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9b30b-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9b30b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b30b-134">OUTPUTS</span></span>

### <span data-ttu-id="9b30b-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9b30b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9b30b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b30b-136">NOTES</span></span>

## <span data-ttu-id="9b30b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b30b-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b30b-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9b30b-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9b30b-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b30b-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9b30b-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b30b-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9b30b-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9b30b-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
