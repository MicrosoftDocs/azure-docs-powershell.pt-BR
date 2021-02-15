---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116228"
---
# <span data-ttu-id="fb2c4-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fb2c4-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="fb2c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2c4-103">Remove um mapeamento de conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="fb2c4-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="fb2c4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb2c4-104">SYNTAX</span></span>

### <span data-ttu-id="fb2c4-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb2c4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb2c4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb2c4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb2c4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb2c4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb2c4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb2c4-108">DESCRIPTION</span></span>
<span data-ttu-id="fb2c4-109">O cmdlet **Remove-AzDataShareDataSetMapping** remove um mapeamentos de conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="fb2c4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb2c4-110">EXAMPLES</span></span>

### <span data-ttu-id="fb2c4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb2c4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="fb2c4-112">Esses comandos removem o grupo de dados chamado DSM do WikiAds de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="fb2c4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb2c4-113">PARAMETERS</span></span>

### <span data-ttu-id="fb2c4-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="fb2c4-114">-AccountName</span></span>
<span data-ttu-id="fb2c4-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-115">Azure data share account name</span></span>

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

### <span data-ttu-id="fb2c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2c4-116">-DefaultProfile</span></span>
<span data-ttu-id="fb2c4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb2c4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb2c4-118">-InputObject</span></span>
<span data-ttu-id="fb2c4-119">O objeto de mapeamento de conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb2c4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb2c4-120">-Name</span></span>
<span data-ttu-id="fb2c4-121">Nome de mapeamento de conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="fb2c4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb2c4-122">-PassThru</span></span>
<span data-ttu-id="fb2c4-123">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="fb2c4-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="fb2c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb2c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb2c4-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fb2c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb2c4-126">-ResourceId</span></span>
<span data-ttu-id="fb2c4-127">A ID do recurso do mapeamento de conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="fb2c4-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fb2c4-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="fb2c4-129">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fb2c4-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="fb2c4-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fb2c4-130">-Confirm</span></span>
<span data-ttu-id="fb2c4-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb2c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2c4-132">-WhatIf</span></span>
<span data-ttu-id="fb2c4-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2c4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb2c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2c4-135">CommonParameters</span></span>
<span data-ttu-id="fb2c4-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2c4-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb2c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2c4-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb2c4-138">INPUTS</span></span>

### <span data-ttu-id="fb2c4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fb2c4-139">System.String</span></span>

### <span data-ttu-id="fb2c4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fb2c4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="fb2c4-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb2c4-141">OUTPUTS</span></span>

### <span data-ttu-id="fb2c4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb2c4-142">System.Boolean</span></span>

## <span data-ttu-id="fb2c4-143">Notas</span><span class="sxs-lookup"><span data-stu-id="fb2c4-143">NOTES</span></span>

## <span data-ttu-id="fb2c4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb2c4-144">RELATED LINKS</span></span>
