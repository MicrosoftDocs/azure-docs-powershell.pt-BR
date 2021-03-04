---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888721"
---
# <span data-ttu-id="0c490-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0c490-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0c490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c490-102">SYNOPSIS</span></span>
<span data-ttu-id="0c490-103">Configura um novo dispositivo de Borda da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="0c490-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="0c490-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c490-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c490-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c490-105">DESCRIPTION</span></span>
<span data-ttu-id="0c490-106">O cmdlet **New-AzDataBoxEdgeDevice** configura um novo dispositivo de Borda de Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="0c490-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="0c490-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c490-107">EXAMPLES</span></span>

### <span data-ttu-id="0c490-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c490-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="0c490-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c490-109">PARAMETERS</span></span>

### <span data-ttu-id="0c490-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c490-110">-AsJob</span></span>
<span data-ttu-id="0c490-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c490-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c490-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c490-112">-DefaultProfile</span></span>
<span data-ttu-id="0c490-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c490-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c490-114">-Location</span><span class="sxs-lookup"><span data-stu-id="0c490-114">-Location</span></span>
<span data-ttu-id="0c490-115">Local do dispositivo</span><span class="sxs-lookup"><span data-stu-id="0c490-115">Location of the device</span></span>

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

### <span data-ttu-id="0c490-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0c490-116">-Name</span></span>
<span data-ttu-id="0c490-117">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="0c490-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c490-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c490-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c490-119">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0c490-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c490-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="0c490-120">-Sku</span></span>
<span data-ttu-id="0c490-121">Skus disponíveis são Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="0c490-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="0c490-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c490-122">-Confirm</span></span>
<span data-ttu-id="0c490-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c490-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c490-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c490-124">-WhatIf</span></span>
<span data-ttu-id="0c490-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c490-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c490-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c490-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c490-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c490-127">CommonParameters</span></span>
<span data-ttu-id="0c490-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c490-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c490-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c490-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c490-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c490-130">INPUTS</span></span>

### <span data-ttu-id="0c490-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0c490-131">None</span></span>

## <span data-ttu-id="0c490-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c490-132">OUTPUTS</span></span>

### <span data-ttu-id="0c490-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0c490-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0c490-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c490-134">NOTES</span></span>

## <span data-ttu-id="0c490-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c490-135">RELATED LINKS</span></span>
