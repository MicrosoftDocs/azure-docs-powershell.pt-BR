---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125520"
---
# <span data-ttu-id="45e59-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="45e59-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="45e59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45e59-102">SYNOPSIS</span></span>
<span data-ttu-id="45e59-103">Configura um novo dispositivo de borda de pilha</span><span class="sxs-lookup"><span data-stu-id="45e59-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="45e59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45e59-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e59-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45e59-105">DESCRIPTION</span></span>
<span data-ttu-id="45e59-106">O cmdlet **New-AzStackEdgeDevice** configura um novo dispositivo de borda de pilha</span><span class="sxs-lookup"><span data-stu-id="45e59-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="45e59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45e59-107">EXAMPLES</span></span>

### <span data-ttu-id="45e59-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45e59-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="45e59-109">OS</span><span class="sxs-lookup"><span data-stu-id="45e59-109">PARAMETERS</span></span>

### <span data-ttu-id="45e59-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45e59-110">-AsJob</span></span>
<span data-ttu-id="45e59-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45e59-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45e59-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e59-112">-DefaultProfile</span></span>
<span data-ttu-id="45e59-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45e59-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45e59-114">-Local</span><span class="sxs-lookup"><span data-stu-id="45e59-114">-Location</span></span>
<span data-ttu-id="45e59-115">Localização do dispositivo</span><span class="sxs-lookup"><span data-stu-id="45e59-115">Location of the device</span></span>

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

### <span data-ttu-id="45e59-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="45e59-116">-Name</span></span>
<span data-ttu-id="45e59-117">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="45e59-117">Resource Name</span></span>

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

### <span data-ttu-id="45e59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e59-118">-ResourceGroupName</span></span>
<span data-ttu-id="45e59-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="45e59-119">Resource Group Name</span></span>

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

### <span data-ttu-id="45e59-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="45e59-120">-Sku</span></span>
<span data-ttu-id="45e59-121">As SKUs disponíveis são Edge, gateway</span><span class="sxs-lookup"><span data-stu-id="45e59-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="45e59-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45e59-122">-Confirm</span></span>
<span data-ttu-id="45e59-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e59-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e59-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e59-124">-WhatIf</span></span>
<span data-ttu-id="45e59-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45e59-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45e59-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45e59-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e59-127">CommonParameters</span></span>
<span data-ttu-id="45e59-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e59-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45e59-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e59-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45e59-130">INPUTS</span></span>

### <span data-ttu-id="45e59-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45e59-131">None</span></span>

## <span data-ttu-id="45e59-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45e59-132">OUTPUTS</span></span>

### <span data-ttu-id="45e59-133">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="45e59-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="45e59-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45e59-134">NOTES</span></span>

## <span data-ttu-id="45e59-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45e59-135">RELATED LINKS</span></span>
