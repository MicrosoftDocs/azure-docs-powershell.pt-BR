---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 0a573f8fa293d2c3e4c84eced54c88eb77032970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892292"
---
# <span data-ttu-id="8caf9-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8caf9-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8caf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8caf9-102">SYNOPSIS</span></span>
<span data-ttu-id="8caf9-103">Remove a conta de Armazenamento de Borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8caf9-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="8caf9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8caf9-104">SYNTAX</span></span>

### <span data-ttu-id="8caf9-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8caf9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8caf9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8caf9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8caf9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8caf9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8caf9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8caf9-108">DESCRIPTION</span></span>
<span data-ttu-id="8caf9-109">O cmdlet **Remove-AzStackEdgeStorageAccount** remove uma Conta de Armazenamento de Borda associada para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="8caf9-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="8caf9-110">Você pode especificar o nome da Conta de Armazenamento de Borda a ser removida como um parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8caf9-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="8caf9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8caf9-111">EXAMPLES</span></span>

### <span data-ttu-id="8caf9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8caf9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="8caf9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8caf9-113">PARAMETERS</span></span>

### <span data-ttu-id="8caf9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8caf9-114">-AsJob</span></span>
<span data-ttu-id="8caf9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8caf9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8caf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8caf9-116">-DefaultProfile</span></span>
<span data-ttu-id="8caf9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8caf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8caf9-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8caf9-118">-DeviceName</span></span>
<span data-ttu-id="8caf9-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8caf9-119">Device Name</span></span>

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

### <span data-ttu-id="8caf9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8caf9-120">-InputObject</span></span>
<span data-ttu-id="8caf9-121">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="8caf9-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8caf9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8caf9-122">-Name</span></span>
<span data-ttu-id="8caf9-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="8caf9-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8caf9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8caf9-124">-PassThru</span></span>
<span data-ttu-id="8caf9-125">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8caf9-125">returns true if successful</span></span>

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

### <span data-ttu-id="8caf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8caf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="8caf9-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8caf9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8caf9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8caf9-128">-ResourceId</span></span>
<span data-ttu-id="8caf9-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8caf9-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8caf9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8caf9-130">-Confirm</span></span>
<span data-ttu-id="8caf9-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8caf9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8caf9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8caf9-132">-WhatIf</span></span>
<span data-ttu-id="8caf9-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8caf9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8caf9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8caf9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8caf9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8caf9-135">CommonParameters</span></span>
<span data-ttu-id="8caf9-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8caf9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8caf9-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8caf9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8caf9-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8caf9-138">INPUTS</span></span>

### <span data-ttu-id="8caf9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8caf9-139">System.String</span></span>

### <span data-ttu-id="8caf9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8caf9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8caf9-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8caf9-141">OUTPUTS</span></span>

### <span data-ttu-id="8caf9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8caf9-142">System.Boolean</span></span>

## <span data-ttu-id="8caf9-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="8caf9-143">NOTES</span></span>

## <span data-ttu-id="8caf9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8caf9-144">RELATED LINKS</span></span>
