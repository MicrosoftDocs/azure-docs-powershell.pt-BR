---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262441"
---
# <span data-ttu-id="b4113-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b4113-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="b4113-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4113-102">SYNOPSIS</span></span>
<span data-ttu-id="b4113-103">Remove um compartilhamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4113-103">Removes a share from the device.</span></span>

## <span data-ttu-id="b4113-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4113-104">SYNTAX</span></span>

### <span data-ttu-id="b4113-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4113-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4113-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4113-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4113-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4113-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4113-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4113-108">DESCRIPTION</span></span>
<span data-ttu-id="b4113-109">O cmdlet **Remove-AzStackEdgeEdgeShare** remove os compartilhamentos de borda associados de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="b4113-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="b4113-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4113-110">EXAMPLES</span></span>

### <span data-ttu-id="b4113-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4113-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="b4113-112">OS</span><span class="sxs-lookup"><span data-stu-id="b4113-112">PARAMETERS</span></span>

### <span data-ttu-id="b4113-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4113-113">-AsJob</span></span>
<span data-ttu-id="b4113-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4113-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4113-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4113-115">-DefaultProfile</span></span>
<span data-ttu-id="b4113-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4113-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4113-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4113-117">-DeviceName</span></span>
<span data-ttu-id="b4113-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4113-118">Device Name</span></span>

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

### <span data-ttu-id="b4113-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4113-119">-InputObject</span></span>
<span data-ttu-id="b4113-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="b4113-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4113-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4113-121">-Name</span></span>
<span data-ttu-id="b4113-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="b4113-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4113-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4113-123">-PassThru</span></span>
<span data-ttu-id="b4113-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b4113-124">returns true if successful</span></span>

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

### <span data-ttu-id="b4113-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4113-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4113-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b4113-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b4113-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4113-127">-ResourceId</span></span>
<span data-ttu-id="b4113-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="b4113-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b4113-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4113-129">-Confirm</span></span>
<span data-ttu-id="b4113-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4113-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4113-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4113-131">-WhatIf</span></span>
<span data-ttu-id="b4113-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4113-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4113-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4113-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4113-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4113-134">CommonParameters</span></span>
<span data-ttu-id="b4113-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4113-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4113-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4113-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4113-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4113-137">INPUTS</span></span>

### <span data-ttu-id="b4113-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4113-138">System.String</span></span>

### <span data-ttu-id="b4113-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="b4113-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="b4113-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4113-140">OUTPUTS</span></span>

### <span data-ttu-id="b4113-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4113-141">System.Boolean</span></span>

## <span data-ttu-id="b4113-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4113-142">NOTES</span></span>

## <span data-ttu-id="b4113-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4113-143">RELATED LINKS</span></span>
