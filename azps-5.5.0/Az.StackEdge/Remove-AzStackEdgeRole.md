---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117059"
---
# <span data-ttu-id="ba697-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ba697-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="ba697-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba697-102">SYNOPSIS</span></span>
<span data-ttu-id="ba697-103">Remove a função IoT associada para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba697-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="ba697-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba697-104">SYNTAX</span></span>

### <span data-ttu-id="ba697-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ba697-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba697-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba697-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba697-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba697-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba697-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba697-108">DESCRIPTION</span></span>
<span data-ttu-id="ba697-109">O cmdlet **Remove-AzSt stackEdgeRole** remove a função IoT associada para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="ba697-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="ba697-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba697-110">EXAMPLES</span></span>

### <span data-ttu-id="ba697-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba697-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="ba697-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba697-112">PARAMETERS</span></span>

### <span data-ttu-id="ba697-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba697-113">-AsJob</span></span>
<span data-ttu-id="ba697-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ba697-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba697-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba697-115">-DefaultProfile</span></span>
<span data-ttu-id="ba697-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba697-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba697-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ba697-117">-DeviceName</span></span>
<span data-ttu-id="ba697-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ba697-118">Device Name</span></span>

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

### <span data-ttu-id="ba697-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba697-119">-InputObject</span></span>
<span data-ttu-id="ba697-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="ba697-120">Input Object</span></span>

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

### <span data-ttu-id="ba697-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba697-121">-Name</span></span>
<span data-ttu-id="ba697-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="ba697-122">Resource Name</span></span>

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

### <span data-ttu-id="ba697-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba697-123">-PassThru</span></span>
<span data-ttu-id="ba697-124">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ba697-124">returns true if successful</span></span>

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

### <span data-ttu-id="ba697-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba697-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba697-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ba697-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ba697-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba697-127">-ResourceId</span></span>
<span data-ttu-id="ba697-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba697-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ba697-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ba697-129">-Confirm</span></span>
<span data-ttu-id="ba697-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba697-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba697-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba697-131">-WhatIf</span></span>
<span data-ttu-id="ba697-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ba697-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba697-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba697-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba697-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba697-134">CommonParameters</span></span>
<span data-ttu-id="ba697-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba697-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba697-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba697-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba697-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="ba697-137">INPUTS</span></span>

### <span data-ttu-id="ba697-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ba697-138">System.String</span></span>

### <span data-ttu-id="ba697-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ba697-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="ba697-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="ba697-140">OUTPUTS</span></span>

### <span data-ttu-id="ba697-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ba697-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="ba697-142">Notas</span><span class="sxs-lookup"><span data-stu-id="ba697-142">NOTES</span></span>

## <span data-ttu-id="ba697-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba697-143">RELATED LINKS</span></span>
