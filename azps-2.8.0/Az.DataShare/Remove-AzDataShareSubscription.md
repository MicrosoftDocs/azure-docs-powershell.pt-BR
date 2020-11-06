---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: a2bcfa4232c7e69bdb17a5d56ff7b79373593b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596686"
---
# <span data-ttu-id="b037a-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b037a-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="b037a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b037a-102">SYNOPSIS</span></span>
<span data-ttu-id="b037a-103">Remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b037a-103">removes a share subscription</span></span>

## <span data-ttu-id="b037a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b037a-104">SYNTAX</span></span>

### <span data-ttu-id="b037a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b037a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b037a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b037a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b037a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b037a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b037a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b037a-108">DESCRIPTION</span></span>
<span data-ttu-id="b037a-109">O cmdlet **Remove-AzDataShareSubscription** remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b037a-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="b037a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b037a-110">EXAMPLES</span></span>

### <span data-ttu-id="b037a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b037a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b037a-112">Esses comandos removem um sharesubscription chamado AdsShareSubscription da WikiAds da conta.</span><span class="sxs-lookup"><span data-stu-id="b037a-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="b037a-113">OS</span><span class="sxs-lookup"><span data-stu-id="b037a-113">PARAMETERS</span></span>

### <span data-ttu-id="b037a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b037a-114">-AccountName</span></span>
<span data-ttu-id="b037a-115">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="b037a-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="b037a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b037a-116">-AsJob</span></span>
<span data-ttu-id="b037a-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="b037a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b037a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b037a-118">-DefaultProfile</span></span>
<span data-ttu-id="b037a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b037a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b037a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b037a-120">-InputObject</span></span>
<span data-ttu-id="b037a-121">Objeto de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b037a-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b037a-122">-Name</span></span>
<span data-ttu-id="b037a-123">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b037a-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b037a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b037a-124">-PassThru</span></span>
<span data-ttu-id="b037a-125">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="b037a-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="b037a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b037a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b037a-127">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b037a-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b037a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b037a-128">-ResourceId</span></span>
<span data-ttu-id="b037a-129">A ID do recurso da assinatura do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b037a-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="b037a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b037a-130">-Confirm</span></span>
<span data-ttu-id="b037a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b037a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b037a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b037a-132">-WhatIf</span></span>
<span data-ttu-id="b037a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b037a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b037a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b037a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b037a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b037a-135">CommonParameters</span></span>
<span data-ttu-id="b037a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b037a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b037a-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b037a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b037a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b037a-138">INPUTS</span></span>

### <span data-ttu-id="b037a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b037a-139">System.String</span></span>

### <span data-ttu-id="b037a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b037a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="b037a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b037a-141">OUTPUTS</span></span>

### <span data-ttu-id="b037a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b037a-142">System.Boolean</span></span>

## <span data-ttu-id="b037a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b037a-143">NOTES</span></span>

## <span data-ttu-id="b037a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b037a-144">RELATED LINKS</span></span>
