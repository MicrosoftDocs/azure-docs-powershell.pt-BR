---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118277"
---
# <span data-ttu-id="921d4-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="921d4-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="921d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="921d4-102">SYNOPSIS</span></span>
<span data-ttu-id="921d4-103">Remove um serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="921d4-103">Removes a private link service</span></span>

## <span data-ttu-id="921d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="921d4-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921d4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="921d4-105">DESCRIPTION</span></span>
<span data-ttu-id="921d4-106">O **cmdlet Remove-AzPrivateLinkService** remove um serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="921d4-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="921d4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="921d4-107">EXAMPLES</span></span>

### <span data-ttu-id="921d4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="921d4-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="921d4-109">Este exemplo remove um serviço de link particular chamado TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="921d4-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="921d4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="921d4-110">PARAMETERS</span></span>

### <span data-ttu-id="921d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="921d4-111">-AsJob</span></span>
<span data-ttu-id="921d4-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="921d4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="921d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921d4-113">-DefaultProfile</span></span>
<span data-ttu-id="921d4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="921d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="921d4-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="921d4-115">-Force</span></span>
<span data-ttu-id="921d4-116">Não peça confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="921d4-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="921d4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="921d4-117">-Name</span></span>
<span data-ttu-id="921d4-118">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="921d4-118">The name of the service.</span></span>

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

### <span data-ttu-id="921d4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="921d4-119">-PassThru</span></span>
<span data-ttu-id="921d4-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="921d4-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="921d4-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="921d4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="921d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="921d4-123">O nome do grupo de recursos do serviço de vinculação particular.</span><span class="sxs-lookup"><span data-stu-id="921d4-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="921d4-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="921d4-124">-Confirm</span></span>
<span data-ttu-id="921d4-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="921d4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921d4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921d4-126">-WhatIf</span></span>
<span data-ttu-id="921d4-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="921d4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921d4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="921d4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921d4-129">CommonParameters</span></span>
<span data-ttu-id="921d4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921d4-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="921d4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921d4-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="921d4-132">INPUTS</span></span>

### <span data-ttu-id="921d4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="921d4-133">System.String</span></span>

## <span data-ttu-id="921d4-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="921d4-134">OUTPUTS</span></span>

### <span data-ttu-id="921d4-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="921d4-135">System.Boolean</span></span>

## <span data-ttu-id="921d4-136">Notas</span><span class="sxs-lookup"><span data-stu-id="921d4-136">NOTES</span></span>

## <span data-ttu-id="921d4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="921d4-137">RELATED LINKS</span></span>

[<span data-ttu-id="921d4-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="921d4-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="921d4-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="921d4-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)