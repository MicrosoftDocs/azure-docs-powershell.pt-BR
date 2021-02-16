---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113293"
---
# <span data-ttu-id="8388f-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8388f-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8388f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8388f-102">SYNOPSIS</span></span>
<span data-ttu-id="8388f-103">Remove um contêiner de armazenamento para a conta de Armazenamento de Borda em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8388f-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="8388f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8388f-104">SYNTAX</span></span>

### <span data-ttu-id="8388f-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8388f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8388f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8388f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8388f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8388f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8388f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8388f-108">DESCRIPTION</span></span>
<span data-ttu-id="8388f-109">O cmdlet **Remove-AzDataBoxEdgeStorageContainer** remove um contêiner de armazenamento associado para a conta de Armazenamento de Borda em um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="8388f-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="8388f-110">Você pode especificar o nome do contêiner de armazenamento a ser removido como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8388f-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="8388f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8388f-111">EXAMPLES</span></span>

### <span data-ttu-id="8388f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8388f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="8388f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8388f-113">PARAMETERS</span></span>

### <span data-ttu-id="8388f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8388f-114">-AsJob</span></span>
<span data-ttu-id="8388f-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8388f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8388f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8388f-116">-DefaultProfile</span></span>
<span data-ttu-id="8388f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8388f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8388f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8388f-118">-DeviceName</span></span>
<span data-ttu-id="8388f-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8388f-119">Device Name</span></span>

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

### <span data-ttu-id="8388f-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8388f-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="8388f-121">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="8388f-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="8388f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8388f-122">-InputObject</span></span>
<span data-ttu-id="8388f-123">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="8388f-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8388f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8388f-124">-Name</span></span>
<span data-ttu-id="8388f-125">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="8388f-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8388f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8388f-126">-PassThru</span></span>
<span data-ttu-id="8388f-127">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8388f-127">returns true if successful</span></span>

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

### <span data-ttu-id="8388f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8388f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8388f-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8388f-129">Resource Group Name</span></span>

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

### <span data-ttu-id="8388f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8388f-130">-ResourceId</span></span>
<span data-ttu-id="8388f-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8388f-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="8388f-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8388f-132">-Confirm</span></span>
<span data-ttu-id="8388f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8388f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8388f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8388f-134">-WhatIf</span></span>
<span data-ttu-id="8388f-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8388f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8388f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8388f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8388f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8388f-137">CommonParameters</span></span>
<span data-ttu-id="8388f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8388f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8388f-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8388f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8388f-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="8388f-140">INPUTS</span></span>

### <span data-ttu-id="8388f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8388f-141">System.String</span></span>

### <span data-ttu-id="8388f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8388f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8388f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8388f-143">OUTPUTS</span></span>

### <span data-ttu-id="8388f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8388f-144">System.Boolean</span></span>

## <span data-ttu-id="8388f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8388f-145">NOTES</span></span>

## <span data-ttu-id="8388f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8388f-146">RELATED LINKS</span></span>
