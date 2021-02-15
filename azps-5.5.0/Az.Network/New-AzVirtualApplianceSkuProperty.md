---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115108"
---
# <span data-ttu-id="76176-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="76176-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="76176-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76176-102">SYNOPSIS</span></span>
<span data-ttu-id="76176-103">Defina uma SKU de Dispositivo Virtual de Rede para o recurso.</span><span class="sxs-lookup"><span data-stu-id="76176-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="76176-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76176-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76176-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="76176-105">DESCRIPTION</span></span>
<span data-ttu-id="76176-106">O New-AzVirtualApplianceSkuProperties define uma SKU para o recurso Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="76176-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="76176-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76176-107">EXAMPLES</span></span>

### <span data-ttu-id="76176-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76176-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="76176-109">Crie um objeto Virtual Appliance SKU Properties para ser usado com New-AzNetworkVirtualAppliance comando.</span><span class="sxs-lookup"><span data-stu-id="76176-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="76176-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76176-110">PARAMETERS</span></span>

### <span data-ttu-id="76176-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="76176-111">-BundledScaleUnit</span></span>
<span data-ttu-id="76176-112">A unidade de escala agrupada.</span><span class="sxs-lookup"><span data-stu-id="76176-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="76176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76176-113">-DefaultProfile</span></span>
<span data-ttu-id="76176-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76176-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76176-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="76176-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="76176-116">A versão de local de mercado.</span><span class="sxs-lookup"><span data-stu-id="76176-116">The market place version.</span></span>

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

### <span data-ttu-id="76176-117">-Nomedo Fornecedor</span><span class="sxs-lookup"><span data-stu-id="76176-117">-VendorName</span></span>
<span data-ttu-id="76176-118">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="76176-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="76176-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76176-119">CommonParameters</span></span>
<span data-ttu-id="76176-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76176-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76176-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76176-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76176-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="76176-122">INPUTS</span></span>

### <span data-ttu-id="76176-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="76176-123">None</span></span>

## <span data-ttu-id="76176-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="76176-124">OUTPUTS</span></span>

### <span data-ttu-id="76176-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="76176-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="76176-126">Notas</span><span class="sxs-lookup"><span data-stu-id="76176-126">NOTES</span></span>

## <span data-ttu-id="76176-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76176-127">RELATED LINKS</span></span>
