---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886977"
---
# <span data-ttu-id="52965-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="52965-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="52965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52965-102">SYNOPSIS</span></span>
<span data-ttu-id="52965-103">Remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="52965-103">Removes a data share.</span></span>

## <span data-ttu-id="52965-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52965-104">SYNTAX</span></span>

### <span data-ttu-id="52965-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52965-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52965-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52965-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52965-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52965-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52965-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52965-108">DESCRIPTION</span></span>
<span data-ttu-id="52965-109">O cmdlet **Remove-AzDataShare** remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="52965-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="52965-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52965-110">EXAMPLES</span></span>

### <span data-ttu-id="52965-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52965-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="52965-112">Esses comandos removem o compartilhamento de dados chamado AdsShare da conta de compartilhamento de dados do azure WikiAds.</span><span class="sxs-lookup"><span data-stu-id="52965-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="52965-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52965-113">PARAMETERS</span></span>

### <span data-ttu-id="52965-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52965-114">-AccountName</span></span>
<span data-ttu-id="52965-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="52965-115">Azure data share account name</span></span>

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

### <span data-ttu-id="52965-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52965-116">-AsJob</span></span>
<span data-ttu-id="52965-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="52965-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="52965-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52965-118">-DefaultProfile</span></span>
<span data-ttu-id="52965-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52965-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52965-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52965-120">-InputObject</span></span>
<span data-ttu-id="52965-121">Objeto de compartilhamento de dados do Azure' ''yaml Tipo: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="52965-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="52965-122">Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: True (ByValue) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="52965-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52965-123">-Name</span><span class="sxs-lookup"><span data-stu-id="52965-123">-Name</span></span>
<span data-ttu-id="52965-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="52965-124">Azure data share name</span></span>

<span data-ttu-id="52965-125">tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="52965-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="52965-126">Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: Caracteres curinga false accept: False</span><span class="sxs-lookup"><span data-stu-id="52965-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52965-127">-PassThru</span></span>
<span data-ttu-id="52965-128">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="52965-128">Return object (if specified).</span></span>

<span data-ttu-id="52965-129">tipo yaml: Conjuntos de parâmetros SwitchParameter: (Todos) Aliases:</span><span class="sxs-lookup"><span data-stu-id="52965-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="52965-130">Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False</span><span class="sxs-lookup"><span data-stu-id="52965-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52965-131">-ResourceGroupName</span></span>
<span data-ttu-id="52965-132">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="52965-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="52965-133">tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByFieldsParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="52965-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="52965-134">Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: Caracteres curinga false accept: False</span><span class="sxs-lookup"><span data-stu-id="52965-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52965-135">-ResourceId</span></span>
<span data-ttu-id="52965-136">A id de recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="52965-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="52965-137">tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByResourceIdParameterSet Aliases:</span><span class="sxs-lookup"><span data-stu-id="52965-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="52965-138">Obrigatório: True Position: Nomeado Valor padrão: Entrada de pipeline Nenhum Aceitar: True (ByPropertyName) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="52965-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52965-139">-Confirm</span></span>
<span data-ttu-id="52965-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52965-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="52965-141">tipo yaml: SwitchParameter Parameter Sets: (All) Aliases: cf</span><span class="sxs-lookup"><span data-stu-id="52965-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="52965-142">Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False</span><span class="sxs-lookup"><span data-stu-id="52965-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52965-143">-WhatIf</span></span>
<span data-ttu-id="52965-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52965-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52965-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52965-145">The cmdlet is not run.</span></span>

<span data-ttu-id="52965-146">tipo yaml: SwitchParameter Parameter Sets: (All) Aliases: wi</span><span class="sxs-lookup"><span data-stu-id="52965-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="52965-147">Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False</span><span class="sxs-lookup"><span data-stu-id="52965-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="52965-148">tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetros ataShare: Aliases ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="52965-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="52965-149">Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: True (ByValue) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="52965-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="52965-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52965-150">CommonParameters</span></span>
<span data-ttu-id="52965-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52965-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52965-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52965-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52965-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52965-153">INPUTS</span></span>

### <span data-ttu-id="52965-154">System.String</span><span class="sxs-lookup"><span data-stu-id="52965-154">System.String</span></span>

### <span data-ttu-id="52965-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="52965-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="52965-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52965-156">OUTPUTS</span></span>

### <span data-ttu-id="52965-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52965-157">System.Boolean</span></span>

## <span data-ttu-id="52965-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="52965-158">NOTES</span></span>

## <span data-ttu-id="52965-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52965-159">RELATED LINKS</span></span>
