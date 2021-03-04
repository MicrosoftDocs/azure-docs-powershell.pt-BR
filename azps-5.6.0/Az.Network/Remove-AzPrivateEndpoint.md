---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 3e1caeb5dec11188cf824bdcddf2b0de78f707c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891116"
---
# <span data-ttu-id="29ab2-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="29ab2-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="29ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="29ab2-103">Remove um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="29ab2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29ab2-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ab2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="29ab2-106">O cmdlet **Remove-AzPrivateEndpoint** remove um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="29ab2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29ab2-107">EXAMPLES</span></span>

### <span data-ttu-id="29ab2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29ab2-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="29ab2-109">Este exemplo remove um ponto de extremidade privado chamado MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="29ab2-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="29ab2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29ab2-110">PARAMETERS</span></span>

### <span data-ttu-id="29ab2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29ab2-111">-AsJob</span></span>
<span data-ttu-id="29ab2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="29ab2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29ab2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ab2-113">-DefaultProfile</span></span>
<span data-ttu-id="29ab2-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29ab2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29ab2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29ab2-115">-Force</span></span>
<span data-ttu-id="29ab2-116">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="29ab2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="29ab2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="29ab2-117">-Name</span></span>
<span data-ttu-id="29ab2-118">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="29ab2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29ab2-119">-PassThru</span></span>
<span data-ttu-id="29ab2-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="29ab2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29ab2-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="29ab2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29ab2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ab2-122">-ResourceGroupName</span></span>
<span data-ttu-id="29ab2-123">O nome do grupo de recursos do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="29ab2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29ab2-124">-Confirm</span></span>
<span data-ttu-id="29ab2-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29ab2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ab2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ab2-126">-WhatIf</span></span>
<span data-ttu-id="29ab2-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ab2-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29ab2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ab2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ab2-129">CommonParameters</span></span>
<span data-ttu-id="29ab2-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ab2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ab2-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29ab2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ab2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29ab2-132">INPUTS</span></span>

### <span data-ttu-id="29ab2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="29ab2-133">System.String</span></span>

## <span data-ttu-id="29ab2-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29ab2-134">OUTPUTS</span></span>

### <span data-ttu-id="29ab2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29ab2-135">System.Boolean</span></span>

## <span data-ttu-id="29ab2-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="29ab2-136">NOTES</span></span>

## <span data-ttu-id="29ab2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29ab2-137">RELATED LINKS</span></span>

[<span data-ttu-id="29ab2-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="29ab2-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="29ab2-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="29ab2-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)