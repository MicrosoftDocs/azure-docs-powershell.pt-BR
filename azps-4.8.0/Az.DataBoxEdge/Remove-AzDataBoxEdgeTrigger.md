---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114183"
---
# <span data-ttu-id="4fb63-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="4fb63-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="4fb63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fb63-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb63-103">Remove um gatilho existente no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fb63-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="4fb63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fb63-104">SYNTAX</span></span>

### <span data-ttu-id="4fb63-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fb63-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb63-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fb63-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb63-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fb63-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fb63-108">DESCRIPTION</span></span>
<span data-ttu-id="4fb63-109">O cmdlet **Remove-AzDataBoxEdgeTrigger** remove um gatilho existente no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="4fb63-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="4fb63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fb63-110">EXAMPLES</span></span>

### <span data-ttu-id="4fb63-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fb63-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="4fb63-112">OS</span><span class="sxs-lookup"><span data-stu-id="4fb63-112">PARAMETERS</span></span>

### <span data-ttu-id="4fb63-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fb63-113">-AsJob</span></span>
<span data-ttu-id="4fb63-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4fb63-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fb63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb63-115">-DefaultProfile</span></span>
<span data-ttu-id="4fb63-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fb63-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4fb63-117">-DeviceName</span></span>
<span data-ttu-id="4fb63-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4fb63-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fb63-119">-InputObject</span></span>
<span data-ttu-id="4fb63-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="4fb63-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb63-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fb63-121">-Name</span></span>
<span data-ttu-id="4fb63-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="4fb63-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb63-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fb63-123">-PassThru</span></span>
<span data-ttu-id="4fb63-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4fb63-124">returns true if successful</span></span>

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

### <span data-ttu-id="4fb63-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb63-125">-ResourceGroupName</span></span>
<span data-ttu-id="4fb63-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4fb63-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb63-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fb63-127">-ResourceId</span></span>
<span data-ttu-id="4fb63-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="4fb63-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb63-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fb63-129">-Confirm</span></span>
<span data-ttu-id="4fb63-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fb63-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb63-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb63-131">-WhatIf</span></span>
<span data-ttu-id="4fb63-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fb63-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fb63-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fb63-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb63-134">CommonParameters</span></span>
<span data-ttu-id="4fb63-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb63-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fb63-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb63-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fb63-137">INPUTS</span></span>

### <span data-ttu-id="4fb63-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4fb63-138">System.String</span></span>

### <span data-ttu-id="4fb63-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="4fb63-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="4fb63-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fb63-140">OUTPUTS</span></span>

### <span data-ttu-id="4fb63-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fb63-141">System.Boolean</span></span>

## <span data-ttu-id="4fb63-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fb63-142">NOTES</span></span>

## <span data-ttu-id="4fb63-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fb63-143">RELATED LINKS</span></span>
