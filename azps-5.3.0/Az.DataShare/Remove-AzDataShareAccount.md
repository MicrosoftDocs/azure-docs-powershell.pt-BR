---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271463"
---
# <span data-ttu-id="81439-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="81439-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="81439-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81439-102">SYNOPSIS</span></span>
<span data-ttu-id="81439-103">Remove uma conta de compartilhamento de DataShare</span><span class="sxs-lookup"><span data-stu-id="81439-103">Removes a datashare account</span></span>

## <span data-ttu-id="81439-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81439-104">SYNTAX</span></span>

### <span data-ttu-id="81439-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="81439-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81439-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81439-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81439-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81439-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81439-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81439-108">DESCRIPTION</span></span>
<span data-ttu-id="81439-109">O cmdlet **Remove-AzDataShareAccount** remove uma conta de compartilhamento de DataShare.</span><span class="sxs-lookup"><span data-stu-id="81439-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="81439-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81439-110">EXAMPLES</span></span>

### <span data-ttu-id="81439-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81439-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="81439-112">Esse comando Remove a conta de compartilhamento de WikiADS do grupo de recursos chamado anúncios.</span><span class="sxs-lookup"><span data-stu-id="81439-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="81439-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="81439-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="81439-114">OS</span><span class="sxs-lookup"><span data-stu-id="81439-114">PARAMETERS</span></span>

### <span data-ttu-id="81439-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81439-115">-AsJob</span></span>
<span data-ttu-id="81439-116">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="81439-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="81439-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81439-117">-DefaultProfile</span></span>
<span data-ttu-id="81439-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81439-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81439-119">-Force</span><span class="sxs-lookup"><span data-stu-id="81439-119">-Force</span></span>
<span data-ttu-id="81439-120">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="81439-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="81439-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81439-121">-InputObject</span></span>
<span data-ttu-id="81439-122">O objeto da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="81439-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81439-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="81439-123">-Name</span></span>
<span data-ttu-id="81439-124">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="81439-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="81439-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81439-125">-PassThru</span></span>
<span data-ttu-id="81439-126">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="81439-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="81439-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81439-127">-ResourceGroupName</span></span>
<span data-ttu-id="81439-128">O nome do grupo de recursos da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="81439-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="81439-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81439-129">-ResourceId</span></span>
<span data-ttu-id="81439-130">A ID do recurso da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="81439-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="81439-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81439-131">-Confirm</span></span>
<span data-ttu-id="81439-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81439-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81439-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81439-133">-WhatIf</span></span>
<span data-ttu-id="81439-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81439-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81439-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81439-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81439-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81439-136">CommonParameters</span></span>
<span data-ttu-id="81439-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81439-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81439-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81439-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81439-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81439-139">INPUTS</span></span>

### <span data-ttu-id="81439-140">System. String</span><span class="sxs-lookup"><span data-stu-id="81439-140">System.String</span></span>

### <span data-ttu-id="81439-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="81439-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="81439-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81439-142">OUTPUTS</span></span>

### <span data-ttu-id="81439-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81439-143">System.Boolean</span></span>

## <span data-ttu-id="81439-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81439-144">NOTES</span></span>

## <span data-ttu-id="81439-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81439-145">RELATED LINKS</span></span>
