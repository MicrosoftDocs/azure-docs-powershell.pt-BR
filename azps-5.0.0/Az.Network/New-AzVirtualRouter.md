---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116400"
---
# <span data-ttu-id="88b2c-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="88b2c-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="88b2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="88b2c-103">Cria um VirtualRouter do Azure.</span><span class="sxs-lookup"><span data-stu-id="88b2c-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="88b2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88b2c-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88b2c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="88b2c-106">O cmdlet **New-AzVirtualRouter** cria um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="88b2c-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="88b2c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88b2c-107">EXAMPLES</span></span>

### <span data-ttu-id="88b2c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88b2c-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="88b2c-109">OS</span><span class="sxs-lookup"><span data-stu-id="88b2c-109">PARAMETERS</span></span>

### <span data-ttu-id="88b2c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88b2c-110">-AsJob</span></span>
<span data-ttu-id="88b2c-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="88b2c-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b2c-112">-DefaultProfile</span></span>
<span data-ttu-id="88b2c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88b2c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b2c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="88b2c-114">-Force</span></span>
<span data-ttu-id="88b2c-115">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="88b2c-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="88b2c-116">-HostedSubnet</span></span>
<span data-ttu-id="88b2c-117">A sub-rede na qual o roteador virtual está hospedado.</span><span class="sxs-lookup"><span data-stu-id="88b2c-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="88b2c-118">-Local</span><span class="sxs-lookup"><span data-stu-id="88b2c-118">-Location</span></span>
<span data-ttu-id="88b2c-119">O local.</span><span class="sxs-lookup"><span data-stu-id="88b2c-119">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="88b2c-120">-Name</span></span>
<span data-ttu-id="88b2c-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="88b2c-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="88b2c-123">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="88b2c-123">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="88b2c-124">-Tag</span></span>
<span data-ttu-id="88b2c-125">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="88b2c-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b2c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88b2c-126">-Confirm</span></span>
<span data-ttu-id="88b2c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b2c-128">-WhatIf</span></span>
<span data-ttu-id="88b2c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88b2c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b2c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88b2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b2c-131">CommonParameters</span></span>
<span data-ttu-id="88b2c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b2c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b2c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b2c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88b2c-134">INPUTS</span></span>

### <span data-ttu-id="88b2c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="88b2c-135">System.String</span></span>

### <span data-ttu-id="88b2c-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88b2c-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88b2c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88b2c-137">OUTPUTS</span></span>

### <span data-ttu-id="88b2c-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="88b2c-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="88b2c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88b2c-139">NOTES</span></span>

## <span data-ttu-id="88b2c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88b2c-140">RELATED LINKS</span></span>
