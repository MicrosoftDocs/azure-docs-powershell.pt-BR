---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434689"
---
# <span data-ttu-id="abae2-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abae2-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="abae2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abae2-102">SYNOPSIS</span></span>
<span data-ttu-id="abae2-103">Remove um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="abae2-103">Removes a private link service</span></span>

## <span data-ttu-id="abae2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abae2-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abae2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abae2-105">DESCRIPTION</span></span>
<span data-ttu-id="abae2-106">O cmdlet **Remove-AzPrivateLinkService** remove um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="abae2-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="abae2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abae2-107">EXAMPLES</span></span>

### <span data-ttu-id="abae2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abae2-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="abae2-109">Este exemplo remove um serviço de link particular chamado TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="abae2-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="abae2-110">OS</span><span class="sxs-lookup"><span data-stu-id="abae2-110">PARAMETERS</span></span>

### <span data-ttu-id="abae2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abae2-111">-AsJob</span></span>
<span data-ttu-id="abae2-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="abae2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abae2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abae2-113">-DefaultProfile</span></span>
<span data-ttu-id="abae2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abae2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abae2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="abae2-115">-Force</span></span>
<span data-ttu-id="abae2-116">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="abae2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="abae2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="abae2-117">-Name</span></span>
<span data-ttu-id="abae2-118">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="abae2-118">The name of the service.</span></span>

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

### <span data-ttu-id="abae2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abae2-119">-PassThru</span></span>
<span data-ttu-id="abae2-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="abae2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="abae2-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="abae2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="abae2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abae2-122">-ResourceGroupName</span></span>
<span data-ttu-id="abae2-123">O nome do grupo de recursos do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="abae2-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="abae2-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abae2-124">-Confirm</span></span>
<span data-ttu-id="abae2-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abae2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abae2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abae2-126">-WhatIf</span></span>
<span data-ttu-id="abae2-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abae2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abae2-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abae2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abae2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abae2-129">CommonParameters</span></span>
<span data-ttu-id="abae2-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abae2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abae2-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abae2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abae2-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abae2-132">INPUTS</span></span>

### <span data-ttu-id="abae2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="abae2-133">System.String</span></span>

## <span data-ttu-id="abae2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abae2-134">OUTPUTS</span></span>

### <span data-ttu-id="abae2-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abae2-135">System.Boolean</span></span>

## <span data-ttu-id="abae2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abae2-136">NOTES</span></span>

## <span data-ttu-id="abae2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abae2-137">RELATED LINKS</span></span>

[<span data-ttu-id="abae2-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abae2-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="abae2-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abae2-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)