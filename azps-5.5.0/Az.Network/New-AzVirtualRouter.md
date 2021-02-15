---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117368"
---
# <span data-ttu-id="fc7b1-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fc7b1-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="fc7b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7b1-103">Cria uma Rota Virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="fc7b1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc7b1-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7b1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc7b1-106">O **cmdlet New-AzVirtualRouter** cria um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fc7b1-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="fc7b1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7b1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc7b1-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="fc7b1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc7b1-109">PARAMETERS</span></span>

### <span data-ttu-id="fc7b1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc7b1-110">-AsJob</span></span>
<span data-ttu-id="fc7b1-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fc7b1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc7b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7b1-112">-DefaultProfile</span></span>
<span data-ttu-id="fc7b1-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7b1-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="fc7b1-114">-Force</span></span>
<span data-ttu-id="fc7b1-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="fc7b1-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fc7b1-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="fc7b1-116">-HostedSubnet</span></span>
<span data-ttu-id="fc7b1-117">A sub-rede onde o roteador virtual está hospedado.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="fc7b1-118">-Local</span><span class="sxs-lookup"><span data-stu-id="fc7b1-118">-Location</span></span>
<span data-ttu-id="fc7b1-119">O local.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-119">The location.</span></span>

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

### <span data-ttu-id="fc7b1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc7b1-120">-Name</span></span>
<span data-ttu-id="fc7b1-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="fc7b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc7b1-123">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="fc7b1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc7b1-124">-Tag</span></span>
<span data-ttu-id="fc7b1-125">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fc7b1-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fc7b1-126">-Confirm</span></span>
<span data-ttu-id="fc7b1-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7b1-128">-WhatIf</span></span>
<span data-ttu-id="fc7b1-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7b1-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7b1-131">CommonParameters</span></span>
<span data-ttu-id="fc7b1-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7b1-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc7b1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7b1-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="fc7b1-134">INPUTS</span></span>

### <span data-ttu-id="fc7b1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fc7b1-135">System.String</span></span>

### <span data-ttu-id="fc7b1-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc7b1-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc7b1-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="fc7b1-137">OUTPUTS</span></span>

### <span data-ttu-id="fc7b1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fc7b1-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="fc7b1-139">Notas</span><span class="sxs-lookup"><span data-stu-id="fc7b1-139">NOTES</span></span>

## <span data-ttu-id="fc7b1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc7b1-140">RELATED LINKS</span></span>
