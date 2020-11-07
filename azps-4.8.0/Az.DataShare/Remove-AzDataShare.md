---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948340"
---
# <span data-ttu-id="2ec04-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="2ec04-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="2ec04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ec04-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec04-103">Remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="2ec04-103">Removes a data share.</span></span>

## <span data-ttu-id="2ec04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ec04-104">SYNTAX</span></span>

### <span data-ttu-id="2ec04-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ec04-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec04-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec04-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec04-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec04-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ec04-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec04-109">O cmdlet **Remove-AzDataShare** remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="2ec04-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="2ec04-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ec04-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec04-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ec04-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2ec04-112">Esses comandos removem o compartilhamento de dados chamado AdsShare da conta do Azure data share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="2ec04-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="2ec04-113">OS</span><span class="sxs-lookup"><span data-stu-id="2ec04-113">PARAMETERS</span></span>

### <span data-ttu-id="2ec04-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ec04-114">-AccountName</span></span>
<span data-ttu-id="2ec04-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2ec04-115">Azure data share account name</span></span>

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

### <span data-ttu-id="2ec04-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ec04-116">-AsJob</span></span>
<span data-ttu-id="2ec04-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="2ec04-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2ec04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec04-118">-DefaultProfile</span></span>
<span data-ttu-id="2ec04-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec04-120">-InputObject</span></span>
<span data-ttu-id="2ec04-121">O objeto de compartilhamento de dados do Azure ' ' ' YAML o tipo de parâmetro PSDataShare: ByObjectParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="2ec04-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="2ec04-122">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="2ec04-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ec04-123">-Name</span></span>
<span data-ttu-id="2ec04-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2ec04-124">Azure data share name</span></span>

<span data-ttu-id="2ec04-125">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="2ec04-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="2ec04-126">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="2ec04-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ec04-127">-PassThru</span></span>
<span data-ttu-id="2ec04-128">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="2ec04-128">Return object (if specified).</span></span>

<span data-ttu-id="2ec04-129">YAML tipo: SwitchParameter parâmetro define: (All) aliases:</span><span class="sxs-lookup"><span data-stu-id="2ec04-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="2ec04-130">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="2ec04-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec04-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ec04-132">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="2ec04-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="2ec04-133">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="2ec04-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="2ec04-134">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="2ec04-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ec04-135">-ResourceId</span></span>
<span data-ttu-id="2ec04-136">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2ec04-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="2ec04-137">YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByResourceIdParameterSet aliases:</span><span class="sxs-lookup"><span data-stu-id="2ec04-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="2ec04-138">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByPropertyName) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="2ec04-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ec04-139">-Confirm</span></span>
<span data-ttu-id="2ec04-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ec04-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="2ec04-141">YAML tipo: SwitchParameter parâmetro define: (All) aliases: FC</span><span class="sxs-lookup"><span data-stu-id="2ec04-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="2ec04-142">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="2ec04-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec04-143">-WhatIf</span></span>
<span data-ttu-id="2ec04-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ec04-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec04-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ec04-145">The cmdlet is not run.</span></span>

<span data-ttu-id="2ec04-146">YAML tipo: SwitchParameter parâmetro define: (All) aliases: Wi</span><span class="sxs-lookup"><span data-stu-id="2ec04-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="2ec04-147">Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso</span><span class="sxs-lookup"><span data-stu-id="2ec04-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="2ec04-148">Tipo de YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetro ataShare: alias ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="2ec04-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="2ec04-149">Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false</span><span class="sxs-lookup"><span data-stu-id="2ec04-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="2ec04-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec04-150">CommonParameters</span></span>
<span data-ttu-id="2ec04-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec04-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec04-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ec04-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec04-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ec04-153">INPUTS</span></span>

### <span data-ttu-id="2ec04-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec04-154">System.String</span></span>

### <span data-ttu-id="2ec04-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2ec04-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2ec04-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ec04-156">OUTPUTS</span></span>

### <span data-ttu-id="2ec04-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ec04-157">System.Boolean</span></span>

## <span data-ttu-id="2ec04-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ec04-158">NOTES</span></span>

## <span data-ttu-id="2ec04-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ec04-159">RELATED LINKS</span></span>
