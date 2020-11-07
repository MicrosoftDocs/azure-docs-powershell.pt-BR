---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 353d4ca1e5f5eebd1cda1ec22d801a73db239963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776768"
---
# <span data-ttu-id="ee4a6-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ee4a6-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ee4a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4a6-103">Configura um novo dispositivo de borda de caixa de dados</span><span class="sxs-lookup"><span data-stu-id="ee4a6-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="ee4a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee4a6-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee4a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4a6-106">O cmdlet **New-AzDataBoxEdgeDevice** configura um novo dispositivo de borda de caixa de dados</span><span class="sxs-lookup"><span data-stu-id="ee4a6-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="ee4a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee4a6-107">EXAMPLES</span></span>

### <span data-ttu-id="ee4a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee4a6-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="ee4a6-109">OS</span><span class="sxs-lookup"><span data-stu-id="ee4a6-109">PARAMETERS</span></span>

### <span data-ttu-id="ee4a6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee4a6-110">-AsJob</span></span>
<span data-ttu-id="ee4a6-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ee4a6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee4a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4a6-112">-DefaultProfile</span></span>
<span data-ttu-id="ee4a6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4a6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4a6-114">-Local</span><span class="sxs-lookup"><span data-stu-id="ee4a6-114">-Location</span></span>
<span data-ttu-id="ee4a6-115">Localização do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ee4a6-115">Location of the device</span></span>

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

### <span data-ttu-id="ee4a6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee4a6-116">-Name</span></span>
<span data-ttu-id="ee4a6-117">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="ee4a6-117">Resource Name</span></span>

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

### <span data-ttu-id="ee4a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee4a6-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ee4a6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ee4a6-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="ee4a6-120">-Sku</span></span>
<span data-ttu-id="ee4a6-121">As SKUs disponíveis são Edge, gateway</span><span class="sxs-lookup"><span data-stu-id="ee4a6-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="ee4a6-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee4a6-122">-Confirm</span></span>
<span data-ttu-id="ee4a6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4a6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4a6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4a6-124">-WhatIf</span></span>
<span data-ttu-id="ee4a6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee4a6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee4a6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee4a6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4a6-127">CommonParameters</span></span>
<span data-ttu-id="ee4a6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4a6-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee4a6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4a6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee4a6-130">INPUTS</span></span>

### <span data-ttu-id="ee4a6-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ee4a6-131">None</span></span>

## <span data-ttu-id="ee4a6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee4a6-132">OUTPUTS</span></span>

### <span data-ttu-id="ee4a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ee4a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="ee4a6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee4a6-134">NOTES</span></span>

## <span data-ttu-id="ee4a6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee4a6-135">RELATED LINKS</span></span>