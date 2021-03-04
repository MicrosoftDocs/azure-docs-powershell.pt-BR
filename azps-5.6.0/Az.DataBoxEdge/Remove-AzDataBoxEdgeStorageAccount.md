---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 44a2cd433b8c0167ff472932d318322d9c932971
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885472"
---
# <span data-ttu-id="9ade2-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ade2-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="9ade2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ade2-102">SYNOPSIS</span></span>
<span data-ttu-id="9ade2-103">Remove a conta de Armazenamento de Borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ade2-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="9ade2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9ade2-104">SYNTAX</span></span>

### <span data-ttu-id="9ade2-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9ade2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ade2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ade2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ade2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ade2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ade2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9ade2-108">DESCRIPTION</span></span>
<span data-ttu-id="9ade2-109">O cmdlet **Remove-AzDataBoxEdgeStorageAccount** remove uma Conta de Armazenamento de Borda associada para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="9ade2-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="9ade2-110">Você pode especificar o nome da Conta de Armazenamento de Borda a ser removida como um parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ade2-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="9ade2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ade2-111">EXAMPLES</span></span>

### <span data-ttu-id="9ade2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ade2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="9ade2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9ade2-113">PARAMETERS</span></span>

### <span data-ttu-id="9ade2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ade2-114">-AsJob</span></span>
<span data-ttu-id="9ade2-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ade2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ade2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ade2-116">-DefaultProfile</span></span>
<span data-ttu-id="9ade2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ade2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ade2-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9ade2-118">-DeviceName</span></span>
<span data-ttu-id="9ade2-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9ade2-119">Device Name</span></span>

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

### <span data-ttu-id="9ade2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ade2-120">-InputObject</span></span>
<span data-ttu-id="9ade2-121">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="9ade2-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ade2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9ade2-122">-Name</span></span>
<span data-ttu-id="9ade2-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="9ade2-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ade2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ade2-124">-PassThru</span></span>
<span data-ttu-id="9ade2-125">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9ade2-125">returns true if successful</span></span>

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

### <span data-ttu-id="9ade2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ade2-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ade2-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9ade2-127">Resource Group Name</span></span>

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

### <span data-ttu-id="9ade2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ade2-128">-ResourceId</span></span>
<span data-ttu-id="9ade2-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ade2-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="9ade2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ade2-130">-Confirm</span></span>
<span data-ttu-id="9ade2-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ade2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ade2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ade2-132">-WhatIf</span></span>
<span data-ttu-id="9ade2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ade2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ade2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ade2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ade2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ade2-135">CommonParameters</span></span>
<span data-ttu-id="9ade2-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ade2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ade2-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ade2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ade2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ade2-138">INPUTS</span></span>

### <span data-ttu-id="9ade2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9ade2-139">System.String</span></span>

### <span data-ttu-id="9ade2-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9ade2-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="9ade2-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9ade2-141">OUTPUTS</span></span>

### <span data-ttu-id="9ade2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ade2-142">System.Boolean</span></span>

## <span data-ttu-id="9ade2-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9ade2-143">NOTES</span></span>

## <span data-ttu-id="9ade2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ade2-144">RELATED LINKS</span></span>
