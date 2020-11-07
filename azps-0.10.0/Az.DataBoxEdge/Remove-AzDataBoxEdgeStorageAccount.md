---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 4d69d14d1129deb1bff580a0e0edfdb922b1544d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776743"
---
# <span data-ttu-id="75421-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75421-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="75421-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75421-102">SYNOPSIS</span></span>
<span data-ttu-id="75421-103">Remove a conta de armazenamento de borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75421-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="75421-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75421-104">SYNTAX</span></span>

### <span data-ttu-id="75421-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75421-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75421-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75421-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75421-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75421-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75421-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75421-108">DESCRIPTION</span></span>
<span data-ttu-id="75421-109">O cmdlet **Remove-AzDataBoxEdgeStorageAccount** remove uma conta de armazenamento de borda associada a um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="75421-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="75421-110">Você pode especificar o nome da conta de armazenamento de borda a ser removida como parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75421-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="75421-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75421-111">EXAMPLES</span></span>

### <span data-ttu-id="75421-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75421-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="75421-113">OS</span><span class="sxs-lookup"><span data-stu-id="75421-113">PARAMETERS</span></span>

### <span data-ttu-id="75421-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75421-114">-AsJob</span></span>
<span data-ttu-id="75421-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="75421-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75421-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75421-116">-DefaultProfile</span></span>
<span data-ttu-id="75421-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75421-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75421-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75421-118">-DeviceName</span></span>
<span data-ttu-id="75421-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="75421-119">Device Name</span></span>

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

### <span data-ttu-id="75421-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75421-120">-InputObject</span></span>
<span data-ttu-id="75421-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="75421-121">Input Object</span></span>

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

### <span data-ttu-id="75421-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="75421-122">-Name</span></span>
<span data-ttu-id="75421-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="75421-123">Resource Name</span></span>

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

### <span data-ttu-id="75421-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75421-124">-PassThru</span></span>
<span data-ttu-id="75421-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="75421-125">returns true if successful</span></span>

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

### <span data-ttu-id="75421-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75421-126">-ResourceGroupName</span></span>
<span data-ttu-id="75421-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75421-127">Resource Group Name</span></span>

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

### <span data-ttu-id="75421-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75421-128">-ResourceId</span></span>
<span data-ttu-id="75421-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="75421-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="75421-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75421-130">-Confirm</span></span>
<span data-ttu-id="75421-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75421-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75421-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75421-132">-WhatIf</span></span>
<span data-ttu-id="75421-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75421-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75421-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75421-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75421-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75421-135">CommonParameters</span></span>
<span data-ttu-id="75421-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75421-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75421-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75421-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75421-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75421-138">INPUTS</span></span>

### <span data-ttu-id="75421-139">System. String</span><span class="sxs-lookup"><span data-stu-id="75421-139">System.String</span></span>

### <span data-ttu-id="75421-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75421-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="75421-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75421-141">OUTPUTS</span></span>

### <span data-ttu-id="75421-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75421-142">System.Boolean</span></span>

## <span data-ttu-id="75421-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75421-143">NOTES</span></span>

## <span data-ttu-id="75421-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75421-144">RELATED LINKS</span></span>
