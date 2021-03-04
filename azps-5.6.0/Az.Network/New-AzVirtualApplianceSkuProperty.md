---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892424"
---
# <span data-ttu-id="03d5b-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="03d5b-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="03d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="03d5b-103">Defina um sku de Dispositivo Virtual de Rede para o recurso.</span><span class="sxs-lookup"><span data-stu-id="03d5b-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="03d5b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03d5b-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03d5b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="03d5b-106">O New-AzVirtualApplianceSkuProperties define um recurso Sku para Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="03d5b-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="03d5b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="03d5b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03d5b-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="03d5b-109">Crie um objeto Virtual Appliance Sku Properties a ser usado com New-AzNetworkVirtualAppliance comando.</span><span class="sxs-lookup"><span data-stu-id="03d5b-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="03d5b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03d5b-110">PARAMETERS</span></span>

### <span data-ttu-id="03d5b-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="03d5b-111">-BundledScaleUnit</span></span>
<span data-ttu-id="03d5b-112">A unidade de escala agrupada.</span><span class="sxs-lookup"><span data-stu-id="03d5b-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="03d5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d5b-113">-DefaultProfile</span></span>
<span data-ttu-id="03d5b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03d5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03d5b-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="03d5b-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="03d5b-116">A versão de mercado.</span><span class="sxs-lookup"><span data-stu-id="03d5b-116">The market place version.</span></span>

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

### <span data-ttu-id="03d5b-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="03d5b-117">-VendorName</span></span>
<span data-ttu-id="03d5b-118">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="03d5b-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="03d5b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d5b-119">CommonParameters</span></span>
<span data-ttu-id="03d5b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d5b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d5b-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03d5b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d5b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03d5b-122">INPUTS</span></span>

### <span data-ttu-id="03d5b-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03d5b-123">None</span></span>

## <span data-ttu-id="03d5b-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03d5b-124">OUTPUTS</span></span>

### <span data-ttu-id="03d5b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="03d5b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="03d5b-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="03d5b-126">NOTES</span></span>

## <span data-ttu-id="03d5b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03d5b-127">RELATED LINKS</span></span>
