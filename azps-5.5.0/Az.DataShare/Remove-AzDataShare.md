---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110982"
---
# <span data-ttu-id="4d8fb-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4d8fb-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="4d8fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8fb-103">Remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-103">Removes a data share.</span></span>

## <span data-ttu-id="4d8fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d8fb-104">SYNTAX</span></span>

### <span data-ttu-id="4d8fb-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d8fb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8fb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8fb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8fb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8fb-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8fb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d8fb-108">DESCRIPTION</span></span>
<span data-ttu-id="4d8fb-109">O **cmdlet Remove-AzDataShare** remove um compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="4d8fb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="4d8fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d8fb-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="4d8fb-112">Esses comandos removem o compartilhamento de dados chamado AdsShare da conta wikiAds do compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="4d8fb-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d8fb-113">PARAMETERS</span></span>

### <span data-ttu-id="4d8fb-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="4d8fb-114">-AccountName</span></span>
<span data-ttu-id="4d8fb-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4d8fb-115">Azure data share account name</span></span>

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

### <span data-ttu-id="4d8fb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d8fb-116">-AsJob</span></span>
<span data-ttu-id="4d8fb-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="4d8fb-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="4d8fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8fb-118">-DefaultProfile</span></span>
<span data-ttu-id="4d8fb-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d8fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d8fb-120">-InputObject</span></span>
<span data-ttu-id="4d8fb-121">Objeto de compartilhamento de dados do Azure' ''tipo yaml: Conjuntos de parâmetros PSDataShare: Aliases byObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="4d8fb-122">Obrigatório: Posição Verdadeira: Valor padrão nomeado: nenhuma entrada de pipeline aceita: Verdadeiro (ByValue) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d8fb-123">-Name</span></span>
<span data-ttu-id="4d8fb-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4d8fb-124">Azure data share name</span></span>

<span data-ttu-id="4d8fb-125">Tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4d8fb-126">Obrigatório: Posição Verdadeira: Valor padrão nomeado: entrada de pipeline Nenhum aceitar: caracteres curinga False Accept: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d8fb-127">-PassThru</span></span>
<span data-ttu-id="4d8fb-128">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="4d8fb-128">Return object (if specified).</span></span>

<span data-ttu-id="4d8fb-129">Tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="4d8fb-130">Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d8fb-131">-ResourceGroupName</span></span>
<span data-ttu-id="4d8fb-132">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="4d8fb-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="4d8fb-133">Tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byFieldsParameterSet:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="4d8fb-134">Obrigatório: Posição Verdadeira: Valor padrão nomeado: entrada de pipeline Nenhum aceitar: caracteres curinga False Accept: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d8fb-135">-ResourceId</span></span>
<span data-ttu-id="4d8fb-136">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4d8fb-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="4d8fb-137">tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byResourceIdParameterSet:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="4d8fb-138">Obrigatório: Posição Verdadeira: Valor padrão nomeado: Nenhuma entrada de pipeline aceita: Verdadeiro (ByPropertyName) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4d8fb-139">-Confirm</span></span>
<span data-ttu-id="4d8fb-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="4d8fb-141">Tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases: cf</span><span class="sxs-lookup"><span data-stu-id="4d8fb-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="4d8fb-142">Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8fb-143">-WhatIf</span></span>
<span data-ttu-id="4d8fb-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d8fb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-145">The cmdlet is not run.</span></span>

<span data-ttu-id="4d8fb-146">tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases: wi</span><span class="sxs-lookup"><span data-stu-id="4d8fb-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="4d8fb-147">Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="4d8fb-148">tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetros ataShare: Aliases byObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="4d8fb-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="4d8fb-149">Obrigatório: Posição Verdadeira: Valor padrão nomeado: nenhuma entrada de pipeline aceita: Verdadeiro (ByValue) Aceitar caracteres curinga: False</span><span class="sxs-lookup"><span data-stu-id="4d8fb-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="4d8fb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8fb-150">CommonParameters</span></span>
<span data-ttu-id="4d8fb-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d8fb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8fb-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d8fb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8fb-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d8fb-153">INPUTS</span></span>

### <span data-ttu-id="4d8fb-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4d8fb-154">System.String</span></span>

### <span data-ttu-id="4d8fb-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4d8fb-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4d8fb-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d8fb-156">OUTPUTS</span></span>

### <span data-ttu-id="4d8fb-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d8fb-157">System.Boolean</span></span>

## <span data-ttu-id="4d8fb-158">Notas</span><span class="sxs-lookup"><span data-stu-id="4d8fb-158">NOTES</span></span>

## <span data-ttu-id="4d8fb-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d8fb-159">RELATED LINKS</span></span>
