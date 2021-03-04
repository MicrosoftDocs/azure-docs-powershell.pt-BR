---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 8ef763300d530c764aefc3fa18c6bbf2a781b4b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887348"
---
# <span data-ttu-id="2c798-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c798-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="2c798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c798-102">SYNOPSIS</span></span>
<span data-ttu-id="2c798-103">Remove um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2c798-103">Removes a Management Group</span></span>

## <span data-ttu-id="2c798-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c798-104">SYNTAX</span></span>

### <span data-ttu-id="2c798-105">GroupOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c798-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c798-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c798-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c798-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c798-107">DESCRIPTION</span></span>
<span data-ttu-id="2c798-108">O cmdlet **Remove-AzManagementGroup** exclui um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2c798-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="2c798-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c798-109">EXAMPLES</span></span>

### <span data-ttu-id="2c798-110">Exemplo 1: Remover um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2c798-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="2c798-111">Exemplo 2: Remover um grupo de gerenciamento canalização do objeto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c798-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="2c798-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c798-112">PARAMETERS</span></span>

### <span data-ttu-id="2c798-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c798-113">-DefaultProfile</span></span>
<span data-ttu-id="2c798-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c798-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c798-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="2c798-115">-GroupName</span></span>
<span data-ttu-id="2c798-116">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2c798-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c798-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c798-117">-InputObject</span></span>
<span data-ttu-id="2c798-118">Objeto Input da chamada Get</span><span class="sxs-lookup"><span data-stu-id="2c798-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c798-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c798-119">-PassThru</span></span>
<span data-ttu-id="2c798-120">Retornar `true` a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="2c798-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2c798-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c798-121">-Confirm</span></span>
<span data-ttu-id="2c798-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c798-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c798-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c798-123">-WhatIf</span></span>
<span data-ttu-id="2c798-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c798-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c798-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c798-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c798-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c798-126">CommonParameters</span></span>
<span data-ttu-id="2c798-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c798-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c798-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c798-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c798-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c798-129">INPUTS</span></span>

### <span data-ttu-id="2c798-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c798-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="2c798-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c798-131">OUTPUTS</span></span>

### <span data-ttu-id="2c798-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c798-132">System.Boolean</span></span>

## <span data-ttu-id="2c798-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c798-133">NOTES</span></span>

## <span data-ttu-id="2c798-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c798-134">RELATED LINKS</span></span>
