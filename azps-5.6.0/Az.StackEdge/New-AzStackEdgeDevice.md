---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: 1ad2719ae67c96088dde968d96ca7104436083e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889135"
---
# <span data-ttu-id="715da-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="715da-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="715da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="715da-102">SYNOPSIS</span></span>
<span data-ttu-id="715da-103">Configura um novo dispositivo de Borda de Pilha</span><span class="sxs-lookup"><span data-stu-id="715da-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="715da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="715da-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="715da-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="715da-105">DESCRIPTION</span></span>
<span data-ttu-id="715da-106">O cmdlet **New-AzStackEdgeDevice** configura um novo dispositivo de Borda de Pilha</span><span class="sxs-lookup"><span data-stu-id="715da-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="715da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="715da-107">EXAMPLES</span></span>

### <span data-ttu-id="715da-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="715da-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="715da-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="715da-109">PARAMETERS</span></span>

### <span data-ttu-id="715da-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="715da-110">-AsJob</span></span>
<span data-ttu-id="715da-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="715da-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="715da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715da-112">-DefaultProfile</span></span>
<span data-ttu-id="715da-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="715da-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715da-114">-Location</span><span class="sxs-lookup"><span data-stu-id="715da-114">-Location</span></span>
<span data-ttu-id="715da-115">Local do dispositivo</span><span class="sxs-lookup"><span data-stu-id="715da-115">Location of the device</span></span>

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

### <span data-ttu-id="715da-116">-Name</span><span class="sxs-lookup"><span data-stu-id="715da-116">-Name</span></span>
<span data-ttu-id="715da-117">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="715da-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715da-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715da-118">-ResourceGroupName</span></span>
<span data-ttu-id="715da-119">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="715da-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715da-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="715da-120">-Sku</span></span>
<span data-ttu-id="715da-121">Skus disponíveis são Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="715da-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="715da-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="715da-122">-Confirm</span></span>
<span data-ttu-id="715da-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="715da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715da-124">-WhatIf</span></span>
<span data-ttu-id="715da-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="715da-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="715da-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="715da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715da-127">CommonParameters</span></span>
<span data-ttu-id="715da-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715da-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="715da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715da-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="715da-130">INPUTS</span></span>

### <span data-ttu-id="715da-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="715da-131">None</span></span>

## <span data-ttu-id="715da-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="715da-132">OUTPUTS</span></span>

### <span data-ttu-id="715da-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="715da-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="715da-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="715da-134">NOTES</span></span>

## <span data-ttu-id="715da-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="715da-135">RELATED LINKS</span></span>
