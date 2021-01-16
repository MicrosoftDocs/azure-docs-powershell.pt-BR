---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258219"
---
# <span data-ttu-id="b438e-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b438e-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="b438e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b438e-102">SYNOPSIS</span></span>
<span data-ttu-id="b438e-103">Remove um mapeamento de DataSet</span><span class="sxs-lookup"><span data-stu-id="b438e-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="b438e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b438e-104">SYNTAX</span></span>

### <span data-ttu-id="b438e-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b438e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b438e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b438e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b438e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b438e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b438e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b438e-108">DESCRIPTION</span></span>
<span data-ttu-id="b438e-109">O cmdlet **Remove-AzDataShareDataSetMapping** remove mapeamentos de DataSet.</span><span class="sxs-lookup"><span data-stu-id="b438e-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="b438e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b438e-110">EXAMPLES</span></span>

### <span data-ttu-id="b438e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b438e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b438e-112">Esses comandos removem o DataSet chamado DSM de sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b438e-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="b438e-113">OS</span><span class="sxs-lookup"><span data-stu-id="b438e-113">PARAMETERS</span></span>

### <span data-ttu-id="b438e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b438e-114">-AccountName</span></span>
<span data-ttu-id="b438e-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b438e-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b438e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b438e-116">-DefaultProfile</span></span>
<span data-ttu-id="b438e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b438e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b438e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b438e-118">-InputObject</span></span>
<span data-ttu-id="b438e-119">O objeto de mapeamento do Azure Data Set</span><span class="sxs-lookup"><span data-stu-id="b438e-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="b438e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b438e-120">-Name</span></span>
<span data-ttu-id="b438e-121">Nome do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b438e-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="b438e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b438e-122">-PassThru</span></span>
<span data-ttu-id="b438e-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="b438e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="b438e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b438e-124">-ResourceGroupName</span></span>
<span data-ttu-id="b438e-125">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b438e-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b438e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b438e-126">-ResourceId</span></span>
<span data-ttu-id="b438e-127">A ID do recurso do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b438e-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="b438e-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b438e-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="b438e-129">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b438e-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b438e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b438e-130">-Confirm</span></span>
<span data-ttu-id="b438e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b438e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b438e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b438e-132">-WhatIf</span></span>
<span data-ttu-id="b438e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b438e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b438e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b438e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b438e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b438e-135">CommonParameters</span></span>
<span data-ttu-id="b438e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b438e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b438e-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b438e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b438e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b438e-138">INPUTS</span></span>

### <span data-ttu-id="b438e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b438e-139">System.String</span></span>

### <span data-ttu-id="b438e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="b438e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="b438e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b438e-141">OUTPUTS</span></span>

### <span data-ttu-id="b438e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b438e-142">System.Boolean</span></span>

## <span data-ttu-id="b438e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b438e-143">NOTES</span></span>

## <span data-ttu-id="b438e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b438e-144">RELATED LINKS</span></span>
