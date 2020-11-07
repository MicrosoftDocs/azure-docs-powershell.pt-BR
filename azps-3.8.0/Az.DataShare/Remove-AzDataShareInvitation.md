---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 19347de88b1b43c41f8ce774630e92dfc3ad592c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942869"
---
# <span data-ttu-id="13cbb-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="13cbb-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="13cbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="13cbb-103">Remove um convite</span><span class="sxs-lookup"><span data-stu-id="13cbb-103">removes an invitation</span></span>

## <span data-ttu-id="13cbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13cbb-104">SYNTAX</span></span>

### <span data-ttu-id="13cbb-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="13cbb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13cbb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13cbb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13cbb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13cbb-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13cbb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13cbb-108">DESCRIPTION</span></span>
<span data-ttu-id="13cbb-109">O cmdlet **Remove-AzDataShareInvitation** remove um convite de compartilhamento de DataShare.</span><span class="sxs-lookup"><span data-stu-id="13cbb-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="13cbb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13cbb-110">EXAMPLES</span></span>

### <span data-ttu-id="13cbb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13cbb-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="13cbb-112">Esses comandos removem um convite chamado ADSInvite do share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="13cbb-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="13cbb-113">OS</span><span class="sxs-lookup"><span data-stu-id="13cbb-113">PARAMETERS</span></span>

### <span data-ttu-id="13cbb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13cbb-114">-AccountName</span></span>
<span data-ttu-id="13cbb-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="13cbb-115">Azure data share account name</span></span>

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

### <span data-ttu-id="13cbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13cbb-116">-DefaultProfile</span></span>
<span data-ttu-id="13cbb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13cbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13cbb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13cbb-118">-InputObject</span></span>
<span data-ttu-id="13cbb-119">Objeto de convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="13cbb-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13cbb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="13cbb-120">-Name</span></span>
<span data-ttu-id="13cbb-121">Nome do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="13cbb-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="13cbb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13cbb-122">-PassThru</span></span>
<span data-ttu-id="13cbb-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="13cbb-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="13cbb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13cbb-124">-ResourceGroupName</span></span>
<span data-ttu-id="13cbb-125">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="13cbb-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="13cbb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13cbb-126">-ResourceId</span></span>
<span data-ttu-id="13cbb-127">A ID do recurso do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="13cbb-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="13cbb-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="13cbb-128">-ShareName</span></span>
<span data-ttu-id="13cbb-129">Nome de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="13cbb-129">Azure data share name.</span></span>

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

### <span data-ttu-id="13cbb-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13cbb-130">-Confirm</span></span>
<span data-ttu-id="13cbb-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13cbb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13cbb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13cbb-132">-WhatIf</span></span>
<span data-ttu-id="13cbb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13cbb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13cbb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13cbb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13cbb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13cbb-135">CommonParameters</span></span>
<span data-ttu-id="13cbb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13cbb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13cbb-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13cbb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13cbb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13cbb-138">INPUTS</span></span>

### <span data-ttu-id="13cbb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13cbb-139">System.String</span></span>

### <span data-ttu-id="13cbb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="13cbb-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="13cbb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13cbb-141">OUTPUTS</span></span>

### <span data-ttu-id="13cbb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13cbb-142">System.Boolean</span></span>

## <span data-ttu-id="13cbb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13cbb-143">NOTES</span></span>

## <span data-ttu-id="13cbb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13cbb-144">RELATED LINKS</span></span>
