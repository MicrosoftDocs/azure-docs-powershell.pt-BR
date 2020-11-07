---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943477"
---
# <span data-ttu-id="75d6f-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="75d6f-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="75d6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="75d6f-103">Remove a função IoT associada a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75d6f-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="75d6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75d6f-104">SYNTAX</span></span>

### <span data-ttu-id="75d6f-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75d6f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75d6f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75d6f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75d6f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75d6f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d6f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="75d6f-109">O cmdlet **Remove-AzStackEdgeRole** remove a função IOT associada a um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="75d6f-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="75d6f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="75d6f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75d6f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="75d6f-112">OS</span><span class="sxs-lookup"><span data-stu-id="75d6f-112">PARAMETERS</span></span>

### <span data-ttu-id="75d6f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75d6f-113">-AsJob</span></span>
<span data-ttu-id="75d6f-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="75d6f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75d6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d6f-115">-DefaultProfile</span></span>
<span data-ttu-id="75d6f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75d6f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d6f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75d6f-117">-DeviceName</span></span>
<span data-ttu-id="75d6f-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="75d6f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75d6f-119">-InputObject</span></span>
<span data-ttu-id="75d6f-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="75d6f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="75d6f-121">-Name</span></span>
<span data-ttu-id="75d6f-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="75d6f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75d6f-123">-PassThru</span></span>
<span data-ttu-id="75d6f-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="75d6f-124">returns true if successful</span></span>

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

### <span data-ttu-id="75d6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="75d6f-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75d6f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75d6f-127">-ResourceId</span></span>
<span data-ttu-id="75d6f-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="75d6f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6f-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75d6f-129">-Confirm</span></span>
<span data-ttu-id="75d6f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d6f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d6f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d6f-131">-WhatIf</span></span>
<span data-ttu-id="75d6f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75d6f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75d6f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75d6f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d6f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d6f-134">CommonParameters</span></span>
<span data-ttu-id="75d6f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d6f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d6f-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75d6f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d6f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75d6f-137">INPUTS</span></span>

### <span data-ttu-id="75d6f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="75d6f-138">System.String</span></span>

### <span data-ttu-id="75d6f-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="75d6f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="75d6f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75d6f-140">OUTPUTS</span></span>

### <span data-ttu-id="75d6f-141">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="75d6f-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="75d6f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75d6f-142">NOTES</span></span>

## <span data-ttu-id="75d6f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75d6f-143">RELATED LINKS</span></span>
