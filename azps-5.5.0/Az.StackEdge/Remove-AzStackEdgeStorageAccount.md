---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118592"
---
# <span data-ttu-id="1300e-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1300e-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="1300e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1300e-102">SYNOPSIS</span></span>
<span data-ttu-id="1300e-103">Remove a conta de Armazenamento de Borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1300e-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="1300e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1300e-104">SYNTAX</span></span>

### <span data-ttu-id="1300e-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1300e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1300e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1300e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1300e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1300e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1300e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1300e-108">DESCRIPTION</span></span>
<span data-ttu-id="1300e-109">O cmdlet **Remove-AzSt stackEdgeStorageAccount** remove uma Conta de Armazenamento de Borda associada para um dispositivo stack edge.</span><span class="sxs-lookup"><span data-stu-id="1300e-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="1300e-110">Você pode especificar o nome da Conta de Armazenamento de Borda a ser removida como um parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1300e-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="1300e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1300e-111">EXAMPLES</span></span>

### <span data-ttu-id="1300e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1300e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="1300e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1300e-113">PARAMETERS</span></span>

### <span data-ttu-id="1300e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1300e-114">-AsJob</span></span>
<span data-ttu-id="1300e-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1300e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1300e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1300e-116">-DefaultProfile</span></span>
<span data-ttu-id="1300e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1300e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1300e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1300e-118">-DeviceName</span></span>
<span data-ttu-id="1300e-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="1300e-119">Device Name</span></span>

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

### <span data-ttu-id="1300e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1300e-120">-InputObject</span></span>
<span data-ttu-id="1300e-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="1300e-121">Input Object</span></span>

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

### <span data-ttu-id="1300e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1300e-122">-Name</span></span>
<span data-ttu-id="1300e-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="1300e-123">Resource Name</span></span>

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

### <span data-ttu-id="1300e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1300e-124">-PassThru</span></span>
<span data-ttu-id="1300e-125">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="1300e-125">returns true if successful</span></span>

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

### <span data-ttu-id="1300e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1300e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1300e-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1300e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="1300e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1300e-128">-ResourceId</span></span>
<span data-ttu-id="1300e-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1300e-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="1300e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1300e-130">-Confirm</span></span>
<span data-ttu-id="1300e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1300e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1300e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1300e-132">-WhatIf</span></span>
<span data-ttu-id="1300e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1300e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1300e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1300e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1300e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1300e-135">CommonParameters</span></span>
<span data-ttu-id="1300e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1300e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1300e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1300e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1300e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="1300e-138">INPUTS</span></span>

### <span data-ttu-id="1300e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1300e-139">System.String</span></span>

### <span data-ttu-id="1300e-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1300e-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="1300e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="1300e-141">OUTPUTS</span></span>

### <span data-ttu-id="1300e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1300e-142">System.Boolean</span></span>

## <span data-ttu-id="1300e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="1300e-143">NOTES</span></span>

## <span data-ttu-id="1300e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1300e-144">RELATED LINKS</span></span>
