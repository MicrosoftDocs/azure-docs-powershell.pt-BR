---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256892"
---
# <span data-ttu-id="d53ad-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="d53ad-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="d53ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d53ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d53ad-103">Remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="d53ad-103">Removes a data share.</span></span>

## <span data-ttu-id="d53ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d53ad-104">SYNTAX</span></span>

### <span data-ttu-id="d53ad-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d53ad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d53ad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d53ad-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d53ad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d53ad-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d53ad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d53ad-108">DESCRIPTION</span></span>
<span data-ttu-id="d53ad-109">O cmdlet **Remove-AzDataShare** remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="d53ad-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="d53ad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d53ad-110">EXAMPLES</span></span>

### <span data-ttu-id="d53ad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d53ad-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d53ad-112">Esses comandos removem o compartilhamento de dados chamado AdsShare da conta do Azure data share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="d53ad-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="d53ad-113">OS</span><span class="sxs-lookup"><span data-stu-id="d53ad-113">PARAMETERS</span></span>

### <span data-ttu-id="d53ad-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d53ad-114">-AccountName</span></span>
<span data-ttu-id="d53ad-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d53ad-115">Azure data share account name</span></span>

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

### <span data-ttu-id="d53ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d53ad-116">-AsJob</span></span>
<span data-ttu-id="d53ad-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="d53ad-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d53ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53ad-118">-DefaultProfile</span></span>
<span data-ttu-id="d53ad-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d53ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d53ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d53ad-120">-InputObject</span></span>
<span data-ttu-id="d53ad-121">O objeto de compartilhamento de dados do Azure ' ' ' YAML o tipo de parâmetro PSDataShare: ByObjectParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="d53ad-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="d53ad-122">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="d53ad-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d53ad-123">-Name</span></span>
<span data-ttu-id="d53ad-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d53ad-124">Azure data share name</span></span>

<span data-ttu-id="d53ad-125">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="d53ad-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="d53ad-126">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="d53ad-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d53ad-127">-PassThru</span></span>
<span data-ttu-id="d53ad-128">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="d53ad-128">Return object (if specified).</span></span>

<span data-ttu-id="d53ad-129">YAML tipo: SwitchParameter parâmetro define: (All) aliases:</span><span class="sxs-lookup"><span data-stu-id="d53ad-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="d53ad-130">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="d53ad-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="d53ad-132">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d53ad-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="d53ad-133">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="d53ad-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="d53ad-134">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="d53ad-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d53ad-135">-ResourceId</span></span>
<span data-ttu-id="d53ad-136">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d53ad-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="d53ad-137">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByResourceIdParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="d53ad-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="d53ad-138">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByPropertyName) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="d53ad-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d53ad-139">-Confirm</span></span>
<span data-ttu-id="d53ad-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d53ad-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="d53ad-141">YAML tipo: SwitchParameter parâmetro define: (All) aliases: FC</span><span class="sxs-lookup"><span data-stu-id="d53ad-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="d53ad-142">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="d53ad-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53ad-143">-WhatIf</span></span>
<span data-ttu-id="d53ad-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d53ad-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53ad-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d53ad-145">The cmdlet is not run.</span></span>

<span data-ttu-id="d53ad-146">YAML tipo: SwitchParameter parâmetro define: (All) aliases: Wi</span><span class="sxs-lookup"><span data-stu-id="d53ad-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="d53ad-147">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="d53ad-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="d53ad-148">Tipo de YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetro ataShare: alias ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="d53ad-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="d53ad-149">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="d53ad-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="d53ad-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53ad-150">CommonParameters</span></span>
<span data-ttu-id="d53ad-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53ad-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53ad-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d53ad-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53ad-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d53ad-153">INPUTS</span></span>

### <span data-ttu-id="d53ad-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d53ad-154">System.String</span></span>

### <span data-ttu-id="d53ad-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d53ad-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d53ad-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d53ad-156">OUTPUTS</span></span>

### <span data-ttu-id="d53ad-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d53ad-157">System.Boolean</span></span>

## <span data-ttu-id="d53ad-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d53ad-158">NOTES</span></span>

## <span data-ttu-id="d53ad-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d53ad-159">RELATED LINKS</span></span>
