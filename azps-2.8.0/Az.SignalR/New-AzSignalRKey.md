---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 4bb121563c0fe7a635caeffe982502bff3468495
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773173"
---
# <span data-ttu-id="dd4de-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="dd4de-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="dd4de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd4de-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4de-103">Regenerar uma tecla de acesso para um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="dd4de-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="dd4de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd4de-104">SYNTAX</span></span>

### <span data-ttu-id="dd4de-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd4de-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4de-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4de-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4de-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4de-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd4de-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd4de-108">DESCRIPTION</span></span>
<span data-ttu-id="dd4de-109">Regenerar uma tecla de acesso para um serviço de sinal de acesso.</span><span class="sxs-lookup"><span data-stu-id="dd4de-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="dd4de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd4de-110">EXAMPLES</span></span>

### <span data-ttu-id="dd4de-111">Regenerar a chave primária</span><span class="sxs-lookup"><span data-stu-id="dd4de-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="dd4de-112">OS</span><span class="sxs-lookup"><span data-stu-id="dd4de-112">PARAMETERS</span></span>

### <span data-ttu-id="dd4de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4de-113">-DefaultProfile</span></span>
<span data-ttu-id="dd4de-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4de-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4de-115">-InputObject</span></span>
<span data-ttu-id="dd4de-116">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="dd4de-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="dd4de-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="dd4de-117">-KeyType</span></span>
<span data-ttu-id="dd4de-118">O tipo de chave, principal ou secundário.</span><span class="sxs-lookup"><span data-stu-id="dd4de-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="dd4de-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd4de-119">-Name</span></span>
<span data-ttu-id="dd4de-120">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="dd4de-120">SignalR service name.</span></span>

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

### <span data-ttu-id="dd4de-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd4de-121">-PassThru</span></span>
<span data-ttu-id="dd4de-122">Retorna verdadeiro se a regeneração foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="dd4de-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="dd4de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4de-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd4de-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd4de-124">Resource group name.</span></span>

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

### <span data-ttu-id="dd4de-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd4de-125">-ResourceId</span></span>
<span data-ttu-id="dd4de-126">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="dd4de-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="dd4de-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd4de-127">-Confirm</span></span>
<span data-ttu-id="dd4de-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4de-129">-WhatIf</span></span>
<span data-ttu-id="dd4de-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd4de-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4de-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd4de-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4de-132">CommonParameters</span></span>
<span data-ttu-id="dd4de-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4de-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd4de-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4de-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd4de-135">INPUTS</span></span>

### <span data-ttu-id="dd4de-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4de-136">System.String</span></span>
### <span data-ttu-id="dd4de-137">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="dd4de-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="dd4de-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd4de-138">OUTPUTS</span></span>

### <span data-ttu-id="dd4de-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd4de-139">System.Boolean</span></span>
## <span data-ttu-id="dd4de-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd4de-140">NOTES</span></span>

## <span data-ttu-id="dd4de-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd4de-141">RELATED LINKS</span></span>