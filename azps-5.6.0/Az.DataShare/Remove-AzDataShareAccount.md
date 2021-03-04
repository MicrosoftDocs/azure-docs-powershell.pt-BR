---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 74651ea4a9a108db9cc3f666ad6f78f494fcd676
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887776"
---
# <span data-ttu-id="475d4-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="475d4-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="475d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475d4-102">SYNOPSIS</span></span>
<span data-ttu-id="475d4-103">Remove uma conta de datashare</span><span class="sxs-lookup"><span data-stu-id="475d4-103">Removes a datashare account</span></span>

## <span data-ttu-id="475d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="475d4-104">SYNTAX</span></span>

### <span data-ttu-id="475d4-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="475d4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="475d4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="475d4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="475d4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="475d4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475d4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="475d4-108">DESCRIPTION</span></span>
<span data-ttu-id="475d4-109">O cmdlet **Remove-AzDataShareAccount** remove uma conta datashare.</span><span class="sxs-lookup"><span data-stu-id="475d4-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="475d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="475d4-110">EXAMPLES</span></span>

### <span data-ttu-id="475d4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="475d4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="475d4-112">Este comando remove a conta de daiade chamada WikiADS do grupo de recursos chamado ADS.</span><span class="sxs-lookup"><span data-stu-id="475d4-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="475d4-113">Este comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="475d4-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="475d4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="475d4-114">PARAMETERS</span></span>

### <span data-ttu-id="475d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="475d4-115">-AsJob</span></span>
<span data-ttu-id="475d4-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="475d4-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="475d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475d4-117">-DefaultProfile</span></span>
<span data-ttu-id="475d4-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="475d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="475d4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="475d4-119">-Force</span></span>
<span data-ttu-id="475d4-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="475d4-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="475d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="475d4-121">-InputObject</span></span>
<span data-ttu-id="475d4-122">O objeto de conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="475d4-122">The azure data share account object.</span></span>


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

### <span data-ttu-id="475d4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="475d4-123">-Name</span></span>
<span data-ttu-id="475d4-124">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="475d4-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="475d4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="475d4-125">-PassThru</span></span>
<span data-ttu-id="475d4-126">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="475d4-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="475d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="475d4-128">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="475d4-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="475d4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="475d4-129">-ResourceId</span></span>
<span data-ttu-id="475d4-130">A id de recurso da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="475d4-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="475d4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="475d4-131">-Confirm</span></span>
<span data-ttu-id="475d4-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="475d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475d4-133">-WhatIf</span></span>
<span data-ttu-id="475d4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="475d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475d4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="475d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475d4-136">CommonParameters</span></span>
<span data-ttu-id="475d4-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475d4-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="475d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475d4-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="475d4-139">INPUTS</span></span>

### <span data-ttu-id="475d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="475d4-140">System.String</span></span>

### <span data-ttu-id="475d4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="475d4-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="475d4-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="475d4-142">OUTPUTS</span></span>

### <span data-ttu-id="475d4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="475d4-143">System.Boolean</span></span>

## <span data-ttu-id="475d4-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="475d4-144">NOTES</span></span>

## <span data-ttu-id="475d4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="475d4-145">RELATED LINKS</span></span>
