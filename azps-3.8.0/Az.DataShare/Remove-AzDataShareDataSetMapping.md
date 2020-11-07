---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3e28b55a77ffb5f8d4ba95743e897628948d15f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942870"
---
# <span data-ttu-id="3d54f-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3d54f-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3d54f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d54f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d54f-103">Remove um mapeamento de DataSet</span><span class="sxs-lookup"><span data-stu-id="3d54f-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="3d54f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d54f-104">SYNTAX</span></span>

### <span data-ttu-id="3d54f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d54f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d54f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d54f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d54f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d54f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d54f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d54f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d54f-109">O cmdlet **Remove-AzDataShareDataSetMapping** remove mapeamentos de DataSet.</span><span class="sxs-lookup"><span data-stu-id="3d54f-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="3d54f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d54f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d54f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d54f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3d54f-112">Esses comandos removem o DataSet chamado DSM de sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="3d54f-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="3d54f-113">OS</span><span class="sxs-lookup"><span data-stu-id="3d54f-113">PARAMETERS</span></span>

### <span data-ttu-id="3d54f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d54f-114">-AccountName</span></span>
<span data-ttu-id="3d54f-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54f-115">Azure data share account name</span></span>

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

### <span data-ttu-id="3d54f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d54f-116">-DefaultProfile</span></span>
<span data-ttu-id="3d54f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d54f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d54f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d54f-118">-InputObject</span></span>
<span data-ttu-id="3d54f-119">O objeto de mapeamento do Azure Data Set</span><span class="sxs-lookup"><span data-stu-id="3d54f-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="3d54f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d54f-120">-Name</span></span>
<span data-ttu-id="3d54f-121">Nome do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54f-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="3d54f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d54f-122">-PassThru</span></span>
<span data-ttu-id="3d54f-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="3d54f-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="3d54f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d54f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d54f-125">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="3d54f-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3d54f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d54f-126">-ResourceId</span></span>
<span data-ttu-id="3d54f-127">A ID do recurso do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54f-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="3d54f-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3d54f-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="3d54f-129">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54f-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3d54f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d54f-130">-Confirm</span></span>
<span data-ttu-id="3d54f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d54f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d54f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d54f-132">-WhatIf</span></span>
<span data-ttu-id="3d54f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d54f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d54f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d54f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d54f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d54f-135">CommonParameters</span></span>
<span data-ttu-id="3d54f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d54f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d54f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d54f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d54f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d54f-138">INPUTS</span></span>

### <span data-ttu-id="3d54f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3d54f-139">System.String</span></span>

### <span data-ttu-id="3d54f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3d54f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3d54f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d54f-141">OUTPUTS</span></span>

### <span data-ttu-id="3d54f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d54f-142">System.Boolean</span></span>

## <span data-ttu-id="3d54f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d54f-143">NOTES</span></span>

## <span data-ttu-id="3d54f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d54f-144">RELATED LINKS</span></span>
