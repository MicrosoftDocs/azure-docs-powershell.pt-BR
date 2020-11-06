---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429496"
---
# <span data-ttu-id="71866-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71866-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="71866-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71866-102">SYNOPSIS</span></span>
<span data-ttu-id="71866-103">Obtém uma rede virtual toque</span><span class="sxs-lookup"><span data-stu-id="71866-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71866-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71866-104">SYNTAX</span></span>

### <span data-ttu-id="71866-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71866-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71866-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71866-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71866-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71866-107">DESCRIPTION</span></span>
<span data-ttu-id="71866-108">O cmdlet **Get-AzureRmVirtualNetworkTap** Obtém um toque de rede virtual do Azure ou uma lista da rede virtual do Azure toca em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71866-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="71866-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71866-109">EXAMPLES</span></span>

### <span data-ttu-id="71866-110">Exemplo 1: obter uma rede virtual, toque em</span><span class="sxs-lookup"><span data-stu-id="71866-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="71866-111">Este comando obtém uma referência de toque do VirtualNetwork para determinado "VirtualTap1" em "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="71866-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="71866-112">OS</span><span class="sxs-lookup"><span data-stu-id="71866-112">PARAMETERS</span></span>

### <span data-ttu-id="71866-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71866-113">-DefaultProfile</span></span>
<span data-ttu-id="71866-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71866-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71866-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="71866-115">-Name</span></span>
<span data-ttu-id="71866-116">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="71866-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71866-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71866-117">-ResourceGroupName</span></span>
<span data-ttu-id="71866-118">O nome do grupo de recursos da rede virtual toque.</span><span class="sxs-lookup"><span data-stu-id="71866-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71866-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71866-119">-ResourceId</span></span>
<span data-ttu-id="71866-120">ResourceId do recurso VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71866-120">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71866-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71866-121">-Confirm</span></span>
<span data-ttu-id="71866-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71866-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71866-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71866-123">-WhatIf</span></span>
<span data-ttu-id="71866-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71866-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71866-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71866-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71866-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71866-126">CommonParameters</span></span>
<span data-ttu-id="71866-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71866-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71866-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71866-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71866-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71866-129">INPUTS</span></span>

### <span data-ttu-id="71866-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71866-130">System.String</span></span>

## <span data-ttu-id="71866-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71866-131">OUTPUTS</span></span>

### <span data-ttu-id="71866-132">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71866-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="71866-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71866-133">NOTES</span></span>

## <span data-ttu-id="71866-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71866-134">RELATED LINKS</span></span>
