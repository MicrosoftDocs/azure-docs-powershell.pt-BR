---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427038"
---
# <span data-ttu-id="b396a-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b396a-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="b396a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b396a-102">SYNOPSIS</span></span>
<span data-ttu-id="b396a-103">Cria uma instância de PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="b396a-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b396a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b396a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b396a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b396a-105">DESCRIPTION</span></span>
<span data-ttu-id="b396a-106">O cmdlet **New-AzureRmApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="b396a-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="b396a-107">Esse comando é usado com o cmdlet **set-AzureRMApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="b396a-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="b396a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b396a-108">EXAMPLES</span></span>

### <span data-ttu-id="b396a-109">Exemplo 1: criar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="b396a-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="b396a-110">Este exemplo cria uma rede virtual e, em seguida, chama o cmdlet **set-AzureRmApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="b396a-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="b396a-111">OS</span><span class="sxs-lookup"><span data-stu-id="b396a-111">PARAMETERS</span></span>

### <span data-ttu-id="b396a-112">-Local</span><span class="sxs-lookup"><span data-stu-id="b396a-112">-Location</span></span>
<span data-ttu-id="b396a-113">Especifica o local da rede virtual em que esse cmdlet cria a instância.</span><span class="sxs-lookup"><span data-stu-id="b396a-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="b396a-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b396a-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b396a-115">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="b396a-115">North Central US</span></span>
- <span data-ttu-id="b396a-116">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="b396a-116">South Central US</span></span>
- <span data-ttu-id="b396a-117">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="b396a-117">Central US</span></span>
- <span data-ttu-id="b396a-118">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="b396a-118">West Europe</span></span>
- <span data-ttu-id="b396a-119">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="b396a-119">North Europe</span></span>
- <span data-ttu-id="b396a-120">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="b396a-120">West US</span></span>
- <span data-ttu-id="b396a-121">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="b396a-121">East US</span></span>
- <span data-ttu-id="b396a-122">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="b396a-122">East US 2</span></span>
- <span data-ttu-id="b396a-123">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="b396a-123">Japan East</span></span>
- <span data-ttu-id="b396a-124">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="b396a-124">Japan West</span></span>
- <span data-ttu-id="b396a-125">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="b396a-125">Brazil South</span></span>
- <span data-ttu-id="b396a-126">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="b396a-126">Southeast Asia</span></span>
- <span data-ttu-id="b396a-127">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="b396a-127">East Asia</span></span>
- <span data-ttu-id="b396a-128">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="b396a-128">Australia East</span></span>
- <span data-ttu-id="b396a-129">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="b396a-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b396a-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="b396a-130">-SubnetResourceId</span></span>
<span data-ttu-id="b396a-131">Especifica a ID do recurso de sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b396a-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b396a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b396a-132">-DefaultProfile</span></span>
<span data-ttu-id="b396a-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b396a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b396a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b396a-134">CommonParameters</span></span>
<span data-ttu-id="b396a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b396a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b396a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b396a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b396a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b396a-137">INPUTS</span></span>

## <span data-ttu-id="b396a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b396a-138">OUTPUTS</span></span>

### <span data-ttu-id="b396a-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b396a-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="b396a-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b396a-140">NOTES</span></span>

## <span data-ttu-id="b396a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b396a-141">RELATED LINKS</span></span>

