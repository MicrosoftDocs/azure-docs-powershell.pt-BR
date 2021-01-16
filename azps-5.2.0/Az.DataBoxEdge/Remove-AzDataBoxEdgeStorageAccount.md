---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260370"
---
# <span data-ttu-id="f0c9a-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0c9a-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="f0c9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c9a-103">Remove a conta de armazenamento de borda de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="f0c9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0c9a-104">SYNTAX</span></span>

### <span data-ttu-id="f0c9a-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f0c9a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c9a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c9a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c9a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c9a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c9a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0c9a-108">DESCRIPTION</span></span>
<span data-ttu-id="f0c9a-109">O cmdlet **Remove-AzDataBoxEdgeStorageAccount** remove uma conta de armazenamento de borda associada a um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="f0c9a-110">Você pode especificar o nome da conta de armazenamento de borda a ser removida como parâmetro no cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="f0c9a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0c9a-111">EXAMPLES</span></span>

### <span data-ttu-id="f0c9a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0c9a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="f0c9a-113">OS</span><span class="sxs-lookup"><span data-stu-id="f0c9a-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0c9a-114">-AsJob</span></span>
<span data-ttu-id="f0c9a-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f0c9a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0c9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c9a-116">-DefaultProfile</span></span>
<span data-ttu-id="f0c9a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c9a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f0c9a-118">-DeviceName</span></span>
<span data-ttu-id="f0c9a-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f0c9a-119">Device Name</span></span>

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

### <span data-ttu-id="f0c9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0c9a-120">-InputObject</span></span>
<span data-ttu-id="f0c9a-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="f0c9a-121">Input Object</span></span>

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

### <span data-ttu-id="f0c9a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0c9a-122">-Name</span></span>
<span data-ttu-id="f0c9a-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="f0c9a-123">Resource Name</span></span>

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

### <span data-ttu-id="f0c9a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c9a-124">-PassThru</span></span>
<span data-ttu-id="f0c9a-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f0c9a-125">returns true if successful</span></span>

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

### <span data-ttu-id="f0c9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f0c9a-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f0c9a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="f0c9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0c9a-128">-ResourceId</span></span>
<span data-ttu-id="f0c9a-129">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="f0c9a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="f0c9a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0c9a-130">-Confirm</span></span>
<span data-ttu-id="f0c9a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c9a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c9a-132">-WhatIf</span></span>
<span data-ttu-id="f0c9a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0c9a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c9a-135">CommonParameters</span></span>
<span data-ttu-id="f0c9a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c9a-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c9a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c9a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0c9a-138">INPUTS</span></span>

### <span data-ttu-id="f0c9a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c9a-139">System.String</span></span>

### <span data-ttu-id="f0c9a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0c9a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="f0c9a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0c9a-141">OUTPUTS</span></span>

### <span data-ttu-id="f0c9a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0c9a-142">System.Boolean</span></span>

## <span data-ttu-id="f0c9a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0c9a-143">NOTES</span></span>

## <span data-ttu-id="f0c9a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0c9a-144">RELATED LINKS</span></span>
