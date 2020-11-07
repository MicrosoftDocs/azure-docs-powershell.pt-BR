---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 1d9566bedbb3e7479f1e9e00c3cc179a225cab2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942868"
---
# <span data-ttu-id="58c7f-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="58c7f-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="58c7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="58c7f-103">Remove um mapeamento de DataSet</span><span class="sxs-lookup"><span data-stu-id="58c7f-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="58c7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c7f-104">SYNTAX</span></span>

### <span data-ttu-id="58c7f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58c7f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c7f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c7f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c7f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c7f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="58c7f-109">O cmdlet **Remove-AzDataShareDataSet** remove um DataSet.</span><span class="sxs-lookup"><span data-stu-id="58c7f-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="58c7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="58c7f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58c7f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="58c7f-112">Esses comandos removem o DataSet chamado DS do share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="58c7f-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="58c7f-113">OS</span><span class="sxs-lookup"><span data-stu-id="58c7f-113">PARAMETERS</span></span>

### <span data-ttu-id="58c7f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58c7f-114">-AccountName</span></span>
<span data-ttu-id="58c7f-115">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="58c7f-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="58c7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c7f-116">-DefaultProfile</span></span>
<span data-ttu-id="58c7f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58c7f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58c7f-118">-InputObject</span></span>
<span data-ttu-id="58c7f-119">O objeto do Azure Data Set.</span><span class="sxs-lookup"><span data-stu-id="58c7f-119">The azure data set object.</span></span>


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

### <span data-ttu-id="58c7f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c7f-120">-Name</span></span>
<span data-ttu-id="58c7f-121">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="58c7f-121">Azure data set name.</span></span>

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

### <span data-ttu-id="58c7f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58c7f-122">-PassThru</span></span>
<span data-ttu-id="58c7f-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="58c7f-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="58c7f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c7f-124">-ResourceGroupName</span></span>
<span data-ttu-id="58c7f-125">O nome do grupo de recursos da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="58c7f-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="58c7f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58c7f-126">-ResourceId</span></span>
<span data-ttu-id="58c7f-127">A ID do recurso do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="58c7f-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="58c7f-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="58c7f-128">-ShareName</span></span>
<span data-ttu-id="58c7f-129">Nome de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="58c7f-129">Azure data share name.</span></span>

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

### <span data-ttu-id="58c7f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58c7f-130">-Confirm</span></span>
<span data-ttu-id="58c7f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c7f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c7f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c7f-132">-WhatIf</span></span>
<span data-ttu-id="58c7f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58c7f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c7f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58c7f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c7f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c7f-135">CommonParameters</span></span>
<span data-ttu-id="58c7f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c7f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c7f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c7f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c7f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58c7f-138">INPUTS</span></span>

### <span data-ttu-id="58c7f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58c7f-139">System.String</span></span>

### <span data-ttu-id="58c7f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="58c7f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="58c7f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58c7f-141">OUTPUTS</span></span>

### <span data-ttu-id="58c7f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58c7f-142">System.Boolean</span></span>

## <span data-ttu-id="58c7f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58c7f-143">NOTES</span></span>

## <span data-ttu-id="58c7f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58c7f-144">RELATED LINKS</span></span>
