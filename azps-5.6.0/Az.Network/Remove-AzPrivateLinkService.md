---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: e06a29422a7abed55dbf1e8508c8715a36cf7d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891113"
---
# <span data-ttu-id="ca9e8-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca9e8-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="ca9e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9e8-103">Remove um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="ca9e8-103">Removes a private link service</span></span>

## <span data-ttu-id="ca9e8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca9e8-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9e8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca9e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9e8-106">O cmdlet **Remove-AzPrivateLinkService** remove um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="ca9e8-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="ca9e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9e8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca9e8-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="ca9e8-109">Este exemplo remove um serviço de link privado chamado TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="ca9e8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-110">PARAMETERS</span></span>

### <span data-ttu-id="ca9e8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca9e8-111">-AsJob</span></span>
<span data-ttu-id="ca9e8-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca9e8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca9e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9e8-113">-DefaultProfile</span></span>
<span data-ttu-id="ca9e8-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca9e8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ca9e8-115">-Force</span></span>
<span data-ttu-id="ca9e8-116">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="ca9e8-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ca9e8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca9e8-117">-Name</span></span>
<span data-ttu-id="ca9e8-118">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9e8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca9e8-119">-PassThru</span></span>
<span data-ttu-id="ca9e8-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca9e8-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca9e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca9e8-123">O nome do grupo de recursos do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="ca9e8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca9e8-124">-Confirm</span></span>
<span data-ttu-id="ca9e8-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9e8-126">-WhatIf</span></span>
<span data-ttu-id="ca9e8-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9e8-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9e8-129">CommonParameters</span></span>
<span data-ttu-id="ca9e8-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9e8-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca9e8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9e8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-132">INPUTS</span></span>

### <span data-ttu-id="ca9e8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ca9e8-133">System.String</span></span>

## <span data-ttu-id="ca9e8-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-134">OUTPUTS</span></span>

### <span data-ttu-id="ca9e8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca9e8-135">System.Boolean</span></span>

## <span data-ttu-id="ca9e8-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca9e8-136">NOTES</span></span>

## <span data-ttu-id="ca9e8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca9e8-137">RELATED LINKS</span></span>

[<span data-ttu-id="ca9e8-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca9e8-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="ca9e8-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca9e8-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)