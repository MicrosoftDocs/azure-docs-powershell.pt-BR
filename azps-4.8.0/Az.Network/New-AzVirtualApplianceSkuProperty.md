---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111552"
---
# <span data-ttu-id="d04d8-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="d04d8-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="d04d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d04d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d04d8-103">Defina uma SKU de dispositivo virtual de rede para o recurso.</span><span class="sxs-lookup"><span data-stu-id="d04d8-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="d04d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d04d8-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d04d8-105">DESCRIPTION</span></span>
<span data-ttu-id="d04d8-106">O comando New-AzVirtualApplianceSkuProperties define um SKU para o recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="d04d8-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d04d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d04d8-107">EXAMPLES</span></span>

### <span data-ttu-id="d04d8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d04d8-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="d04d8-109">Crie um objeto de propriedades de SKU de aparelho virtual para ser usado com o comando New-AzNetworkVirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="d04d8-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="d04d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="d04d8-110">PARAMETERS</span></span>

### <span data-ttu-id="d04d8-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="d04d8-111">-BundledScaleUnit</span></span>
<span data-ttu-id="d04d8-112">A unidade de escala agrupada.</span><span class="sxs-lookup"><span data-stu-id="d04d8-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="d04d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04d8-113">-DefaultProfile</span></span>
<span data-ttu-id="d04d8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d04d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d04d8-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="d04d8-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="d04d8-116">A versão do mercado de lugar.</span><span class="sxs-lookup"><span data-stu-id="d04d8-116">The market place version.</span></span>

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

### <span data-ttu-id="d04d8-117">-Nome_do_Fornecedor</span><span class="sxs-lookup"><span data-stu-id="d04d8-117">-VendorName</span></span>
<span data-ttu-id="d04d8-118">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="d04d8-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d04d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04d8-119">CommonParameters</span></span>
<span data-ttu-id="d04d8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04d8-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d04d8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04d8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d04d8-122">INPUTS</span></span>

### <span data-ttu-id="d04d8-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d04d8-123">None</span></span>

## <span data-ttu-id="d04d8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d04d8-124">OUTPUTS</span></span>

### <span data-ttu-id="d04d8-125">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="d04d8-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="d04d8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d04d8-126">NOTES</span></span>

## <span data-ttu-id="d04d8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d04d8-127">RELATED LINKS</span></span>
