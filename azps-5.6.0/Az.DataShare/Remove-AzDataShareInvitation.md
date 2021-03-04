---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 4736a1b6e8d0a6d34cf1874868596d4139ad5e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891191"
---
# <span data-ttu-id="8bc61-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="8bc61-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="8bc61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc61-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc61-103">remove um convite</span><span class="sxs-lookup"><span data-stu-id="8bc61-103">removes an invitation</span></span>

## <span data-ttu-id="8bc61-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8bc61-104">SYNTAX</span></span>

### <span data-ttu-id="8bc61-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8bc61-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc61-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc61-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc61-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc61-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc61-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8bc61-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc61-109">O cmdlet **Remove-AzDataShareInvitation** remove um convite datashare.</span><span class="sxs-lookup"><span data-stu-id="8bc61-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="8bc61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bc61-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc61-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bc61-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8bc61-112">Esses comandos removem um convite chamado ADSInvite do compartilhamento AdsShare.</span><span class="sxs-lookup"><span data-stu-id="8bc61-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="8bc61-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8bc61-113">PARAMETERS</span></span>

### <span data-ttu-id="8bc61-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8bc61-114">-AccountName</span></span>
<span data-ttu-id="8bc61-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="8bc61-115">Azure data share account name</span></span>

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

### <span data-ttu-id="8bc61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc61-116">-DefaultProfile</span></span>
<span data-ttu-id="8bc61-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc61-118">-InputObject</span></span>
<span data-ttu-id="8bc61-119">Objeto de convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="8bc61-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="8bc61-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8bc61-120">-Name</span></span>
<span data-ttu-id="8bc61-121">Nome do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="8bc61-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="8bc61-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bc61-122">-PassThru</span></span>
<span data-ttu-id="8bc61-123">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="8bc61-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="8bc61-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc61-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bc61-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="8bc61-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8bc61-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc61-126">-ResourceId</span></span>
<span data-ttu-id="8bc61-127">A id de recurso do convite de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="8bc61-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="8bc61-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8bc61-128">-ShareName</span></span>
<span data-ttu-id="8bc61-129">Nome do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc61-129">Azure data share name.</span></span>

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

### <span data-ttu-id="8bc61-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bc61-130">-Confirm</span></span>
<span data-ttu-id="8bc61-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc61-132">-WhatIf</span></span>
<span data-ttu-id="8bc61-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bc61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc61-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bc61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc61-135">CommonParameters</span></span>
<span data-ttu-id="8bc61-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc61-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bc61-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc61-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bc61-138">INPUTS</span></span>

### <span data-ttu-id="8bc61-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc61-139">System.String</span></span>

### <span data-ttu-id="8bc61-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="8bc61-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="8bc61-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8bc61-141">OUTPUTS</span></span>

### <span data-ttu-id="8bc61-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8bc61-142">System.Boolean</span></span>

## <span data-ttu-id="8bc61-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="8bc61-143">NOTES</span></span>

## <span data-ttu-id="8bc61-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bc61-144">RELATED LINKS</span></span>
