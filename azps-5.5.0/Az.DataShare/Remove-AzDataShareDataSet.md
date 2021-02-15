---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115361"
---
# <span data-ttu-id="4c86e-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4c86e-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="4c86e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c86e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c86e-103">Remove um mapeamento de conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="4c86e-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="4c86e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c86e-104">SYNTAX</span></span>

### <span data-ttu-id="4c86e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c86e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c86e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c86e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c86e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c86e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c86e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c86e-108">DESCRIPTION</span></span>
<span data-ttu-id="4c86e-109">O cmdlet **Remove-AzDataShareDataSet** remove um conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c86e-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="4c86e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c86e-110">EXAMPLES</span></span>

### <span data-ttu-id="4c86e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c86e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4c86e-112">Esses comandos removem o grupo de dados chamado DS do compartilhamento de WikiAds.</span><span class="sxs-lookup"><span data-stu-id="4c86e-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="4c86e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c86e-113">PARAMETERS</span></span>

### <span data-ttu-id="4c86e-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="4c86e-114">-AccountName</span></span>
<span data-ttu-id="4c86e-115">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c86e-116">-DefaultProfile</span></span>
<span data-ttu-id="4c86e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c86e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c86e-118">-InputObject</span></span>
<span data-ttu-id="4c86e-119">O objeto de conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c86e-120">-Name</span></span>
<span data-ttu-id="4c86e-121">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c86e-122">-PassThru</span></span>
<span data-ttu-id="4c86e-123">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="4c86e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="4c86e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c86e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c86e-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-125">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c86e-126">-ResourceId</span></span>
<span data-ttu-id="4c86e-127">A ID do recurso do conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-127">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4c86e-128">-ShareName</span></span>
<span data-ttu-id="4c86e-129">Nome do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c86e-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c86e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4c86e-130">-Confirm</span></span>
<span data-ttu-id="4c86e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c86e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c86e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c86e-132">-WhatIf</span></span>
<span data-ttu-id="4c86e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4c86e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c86e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c86e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c86e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c86e-135">CommonParameters</span></span>
<span data-ttu-id="4c86e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c86e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c86e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c86e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c86e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c86e-138">INPUTS</span></span>

### <span data-ttu-id="4c86e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4c86e-139">System.String</span></span>

### <span data-ttu-id="4c86e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4c86e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="4c86e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c86e-141">OUTPUTS</span></span>

### <span data-ttu-id="4c86e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c86e-142">System.Boolean</span></span>

## <span data-ttu-id="4c86e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="4c86e-143">NOTES</span></span>

## <span data-ttu-id="4c86e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c86e-144">RELATED LINKS</span></span>
