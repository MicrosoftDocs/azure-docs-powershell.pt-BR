---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113212"
---
# <span data-ttu-id="8d2a7-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d2a7-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8d2a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2a7-103">Remove a conta de armazenamento de borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="8d2a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d2a7-104">SYNTAX</span></span>

### <span data-ttu-id="8d2a7-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d2a7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2a7-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d2a7-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d2a7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d2a7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2a7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d2a7-108">DESCRIPTION</span></span>
<span data-ttu-id="8d2a7-109">O cmdlet **Remove-AzStackEdgeStorageAccount** remove uma conta de armazenamento de borda associada a um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="8d2a7-110">Você pode especificar o nome da conta de armazenamento de borda a ser removida como parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="8d2a7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d2a7-111">EXAMPLES</span></span>

### <span data-ttu-id="8d2a7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d2a7-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="8d2a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="8d2a7-113">PARAMETERS</span></span>

### <span data-ttu-id="8d2a7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d2a7-114">-AsJob</span></span>
<span data-ttu-id="8d2a7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8d2a7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d2a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2a7-116">-DefaultProfile</span></span>
<span data-ttu-id="8d2a7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2a7-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8d2a7-118">-DeviceName</span></span>
<span data-ttu-id="8d2a7-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8d2a7-119">Device Name</span></span>

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

### <span data-ttu-id="8d2a7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d2a7-120">-InputObject</span></span>
<span data-ttu-id="8d2a7-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="8d2a7-121">Input Object</span></span>

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

### <span data-ttu-id="8d2a7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d2a7-122">-Name</span></span>
<span data-ttu-id="8d2a7-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="8d2a7-123">Resource Name</span></span>

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

### <span data-ttu-id="8d2a7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d2a7-124">-PassThru</span></span>
<span data-ttu-id="8d2a7-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8d2a7-125">returns true if successful</span></span>

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

### <span data-ttu-id="8d2a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d2a7-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8d2a7-127">Resource Group Name</span></span>

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

### <span data-ttu-id="8d2a7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d2a7-128">-ResourceId</span></span>
<span data-ttu-id="8d2a7-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="8d2a7-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="8d2a7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d2a7-130">-Confirm</span></span>
<span data-ttu-id="8d2a7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d2a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2a7-132">-WhatIf</span></span>
<span data-ttu-id="8d2a7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d2a7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d2a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2a7-135">CommonParameters</span></span>
<span data-ttu-id="8d2a7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d2a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2a7-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d2a7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2a7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d2a7-138">INPUTS</span></span>

### <span data-ttu-id="8d2a7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8d2a7-139">System.String</span></span>

### <span data-ttu-id="8d2a7-140">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d2a7-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="8d2a7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d2a7-141">OUTPUTS</span></span>

### <span data-ttu-id="8d2a7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d2a7-142">System.Boolean</span></span>

## <span data-ttu-id="8d2a7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d2a7-143">NOTES</span></span>

## <span data-ttu-id="8d2a7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d2a7-144">RELATED LINKS</span></span>
