---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600563"
---
# <span data-ttu-id="0f465-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f465-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="0f465-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f465-102">SYNOPSIS</span></span>
<span data-ttu-id="0f465-103">O cmdlet Get-AzInterfaceEndpoint Obtém um ponto de extremidade de interface.</span><span class="sxs-lookup"><span data-stu-id="0f465-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="0f465-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f465-104">SYNTAX</span></span>

### <span data-ttu-id="0f465-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f465-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f465-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f465-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f465-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f465-107">DESCRIPTION</span></span>
<span data-ttu-id="0f465-108">O cmdlet **Get-AzInterfaceEndpoint** Obtém um ponto de extremidade de interface.</span><span class="sxs-lookup"><span data-stu-id="0f465-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="0f465-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f465-109">EXAMPLES</span></span>

### <span data-ttu-id="0f465-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f465-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0f465-111">Esse comando obtém o ponto de extremidade da interface chamado InterfaceEndpoint1 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="0f465-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="0f465-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0f465-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="0f465-113">Esse comando obtém o ponto de extremidade da interface com ResourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 e o armazena na variável $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="0f465-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="0f465-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0f465-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="0f465-115">Esse comando obtém os pontos de extremidade da interface que começam com "InterfaceEndpoint"</span><span class="sxs-lookup"><span data-stu-id="0f465-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="0f465-116">OS</span><span class="sxs-lookup"><span data-stu-id="0f465-116">PARAMETERS</span></span>

### <span data-ttu-id="0f465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f465-117">-DefaultProfile</span></span>
<span data-ttu-id="0f465-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f465-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f465-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f465-119">-Name</span></span>
<span data-ttu-id="0f465-120">O nome do ponto de extremidade da interface</span><span class="sxs-lookup"><span data-stu-id="0f465-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0f465-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f465-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f465-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f465-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0f465-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f465-123">-ResourceId</span></span>
<span data-ttu-id="0f465-124">A ID do ponto de extremidade da interface.</span><span class="sxs-lookup"><span data-stu-id="0f465-124">The ID of the interface endpoint.</span></span>

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

### <span data-ttu-id="0f465-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f465-125">-Confirm</span></span>
<span data-ttu-id="0f465-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f465-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f465-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f465-127">-WhatIf</span></span>
<span data-ttu-id="0f465-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f465-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f465-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f465-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f465-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f465-130">CommonParameters</span></span>
<span data-ttu-id="0f465-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f465-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f465-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f465-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f465-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f465-133">INPUTS</span></span>

### <span data-ttu-id="0f465-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f465-134">System.String</span></span>

## <span data-ttu-id="0f465-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f465-135">OUTPUTS</span></span>

### <span data-ttu-id="0f465-136">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f465-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="0f465-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f465-137">NOTES</span></span>

## <span data-ttu-id="0f465-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f465-138">RELATED LINKS</span></span>
