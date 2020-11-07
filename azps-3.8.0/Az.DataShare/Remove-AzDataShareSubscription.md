---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 12298f5c61981cb34572a104d39a279f7024adf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942866"
---
# <span data-ttu-id="d66f2-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d66f2-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="d66f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d66f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d66f2-103">Remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d66f2-103">removes a share subscription</span></span>

## <span data-ttu-id="d66f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d66f2-104">SYNTAX</span></span>

### <span data-ttu-id="d66f2-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d66f2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66f2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d66f2-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66f2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d66f2-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66f2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d66f2-108">DESCRIPTION</span></span>
<span data-ttu-id="d66f2-109">O cmdlet **Remove-AzDataShareSubscription** remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d66f2-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="d66f2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d66f2-110">EXAMPLES</span></span>

### <span data-ttu-id="d66f2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d66f2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d66f2-112">Esses comandos removem um sharesubscription chamado AdsShareSubscription da WikiAds da conta.</span><span class="sxs-lookup"><span data-stu-id="d66f2-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="d66f2-113">OS</span><span class="sxs-lookup"><span data-stu-id="d66f2-113">PARAMETERS</span></span>

### <span data-ttu-id="d66f2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d66f2-114">-AccountName</span></span>
<span data-ttu-id="d66f2-115">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="d66f2-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="d66f2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d66f2-116">-AsJob</span></span>
<span data-ttu-id="d66f2-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="d66f2-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d66f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66f2-118">-DefaultProfile</span></span>
<span data-ttu-id="d66f2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d66f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d66f2-120">-InputObject</span></span>
<span data-ttu-id="d66f2-121">Objeto de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d66f2-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="d66f2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d66f2-122">-Name</span></span>
<span data-ttu-id="d66f2-123">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d66f2-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d66f2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d66f2-124">-PassThru</span></span>
<span data-ttu-id="d66f2-125">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="d66f2-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="d66f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="d66f2-127">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d66f2-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d66f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d66f2-128">-ResourceId</span></span>
<span data-ttu-id="d66f2-129">A ID do recurso da assinatura do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d66f2-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="d66f2-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d66f2-130">-Confirm</span></span>
<span data-ttu-id="d66f2-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d66f2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66f2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66f2-132">-WhatIf</span></span>
<span data-ttu-id="d66f2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d66f2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66f2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d66f2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66f2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66f2-135">CommonParameters</span></span>
<span data-ttu-id="d66f2-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66f2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66f2-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d66f2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66f2-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d66f2-138">INPUTS</span></span>

### <span data-ttu-id="d66f2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d66f2-139">System.String</span></span>

### <span data-ttu-id="d66f2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="d66f2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="d66f2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d66f2-141">OUTPUTS</span></span>

### <span data-ttu-id="d66f2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d66f2-142">System.Boolean</span></span>

## <span data-ttu-id="d66f2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d66f2-143">NOTES</span></span>

## <span data-ttu-id="d66f2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d66f2-144">RELATED LINKS</span></span>
