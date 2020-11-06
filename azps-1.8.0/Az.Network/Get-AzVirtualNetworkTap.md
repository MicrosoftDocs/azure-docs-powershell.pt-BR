---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: df4da43c1a8edf0c3c887e4acdd009593984c048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600465"
---
# <span data-ttu-id="71d96-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="71d96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71d96-102">SYNOPSIS</span></span>
<span data-ttu-id="71d96-103">Obtém uma rede virtual toque</span><span class="sxs-lookup"><span data-stu-id="71d96-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="71d96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71d96-104">SYNTAX</span></span>

### <span data-ttu-id="71d96-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71d96-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d96-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d96-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71d96-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71d96-107">DESCRIPTION</span></span>
<span data-ttu-id="71d96-108">O cmdlet **Get-AzVirtualNetworkTap** Obtém um toque de rede virtual do Azure ou uma lista da rede virtual do Azure toca em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71d96-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="71d96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71d96-109">EXAMPLES</span></span>

### <span data-ttu-id="71d96-110">Exemplo 1: obter uma rede virtual, toque em</span><span class="sxs-lookup"><span data-stu-id="71d96-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="71d96-111">Este comando obtém uma referência de toque do VirtualNetwork para determinado "VirtualTap1" em "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="71d96-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="71d96-112">Exemplo 2: obter todos os toques de redes virtuais usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="71d96-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="71d96-113">Esse comando obtém todas as referências ao VirtualNetwork em que começam com "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="71d96-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="71d96-114">OS</span><span class="sxs-lookup"><span data-stu-id="71d96-114">PARAMETERS</span></span>

### <span data-ttu-id="71d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d96-115">-DefaultProfile</span></span>
<span data-ttu-id="71d96-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71d96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71d96-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="71d96-117">-Name</span></span>
<span data-ttu-id="71d96-118">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="71d96-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="71d96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d96-119">-ResourceGroupName</span></span>
<span data-ttu-id="71d96-120">O nome do grupo de recursos da rede virtual toque.</span><span class="sxs-lookup"><span data-stu-id="71d96-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="71d96-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71d96-121">-ResourceId</span></span>
<span data-ttu-id="71d96-122">ResourceId do recurso VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="71d96-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71d96-123">-Confirm</span></span>
<span data-ttu-id="71d96-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71d96-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d96-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d96-125">-WhatIf</span></span>
<span data-ttu-id="71d96-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71d96-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71d96-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71d96-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d96-128">CommonParameters</span></span>
<span data-ttu-id="71d96-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d96-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71d96-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d96-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71d96-131">INPUTS</span></span>

### <span data-ttu-id="71d96-132">System. String</span><span class="sxs-lookup"><span data-stu-id="71d96-132">System.String</span></span>

## <span data-ttu-id="71d96-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71d96-133">OUTPUTS</span></span>

### <span data-ttu-id="71d96-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="71d96-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71d96-135">NOTES</span></span>

## <span data-ttu-id="71d96-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71d96-136">RELATED LINKS</span></span>

[<span data-ttu-id="71d96-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="71d96-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="71d96-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71d96-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
