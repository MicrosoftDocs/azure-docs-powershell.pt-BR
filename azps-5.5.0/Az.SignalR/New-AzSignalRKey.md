---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116167"
---
# <span data-ttu-id="f6b13-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="f6b13-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="f6b13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6b13-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b13-103">Regenerar uma chave de acesso para um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="f6b13-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f6b13-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6b13-104">SYNTAX</span></span>

### <span data-ttu-id="f6b13-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6b13-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b13-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6b13-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b13-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6b13-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b13-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6b13-108">DESCRIPTION</span></span>
<span data-ttu-id="f6b13-109">Regenerar uma chave de acesso para um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="f6b13-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f6b13-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6b13-110">EXAMPLES</span></span>

### <span data-ttu-id="f6b13-111">Regenerar a chave primária</span><span class="sxs-lookup"><span data-stu-id="f6b13-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="f6b13-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6b13-112">PARAMETERS</span></span>

### <span data-ttu-id="f6b13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b13-113">-DefaultProfile</span></span>
<span data-ttu-id="f6b13-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6b13-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b13-115">-InputObject</span></span>
<span data-ttu-id="f6b13-116">O objeto de recurso signalr.</span><span class="sxs-lookup"><span data-stu-id="f6b13-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b13-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f6b13-117">-KeyType</span></span>
<span data-ttu-id="f6b13-118">O tipo de chave, principal ou secundário.</span><span class="sxs-lookup"><span data-stu-id="f6b13-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b13-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6b13-119">-Name</span></span>
<span data-ttu-id="f6b13-120">Nome do serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="f6b13-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b13-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6b13-121">-PassThru</span></span>
<span data-ttu-id="f6b13-122">Retorna verdadeiro se a recuperação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="f6b13-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="f6b13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b13-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6b13-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6b13-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b13-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6b13-125">-ResourceId</span></span>
<span data-ttu-id="f6b13-126">A ID do recurso de serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="f6b13-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b13-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f6b13-127">-Confirm</span></span>
<span data-ttu-id="f6b13-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6b13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b13-129">-WhatIf</span></span>
<span data-ttu-id="f6b13-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f6b13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b13-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6b13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b13-132">CommonParameters</span></span>
<span data-ttu-id="f6b13-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b13-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6b13-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b13-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6b13-135">INPUTS</span></span>

### <span data-ttu-id="f6b13-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f6b13-136">System.String</span></span>
### <span data-ttu-id="f6b13-137">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f6b13-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="f6b13-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6b13-138">OUTPUTS</span></span>

### <span data-ttu-id="f6b13-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b13-139">System.Boolean</span></span>
## <span data-ttu-id="f6b13-140">Notas</span><span class="sxs-lookup"><span data-stu-id="f6b13-140">NOTES</span></span>

## <span data-ttu-id="f6b13-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6b13-141">RELATED LINKS</span></span>
