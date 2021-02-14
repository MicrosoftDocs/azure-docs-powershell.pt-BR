---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117185"
---
# <span data-ttu-id="6d0b2-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d0b2-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="6d0b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0b2-103">Remove um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d0b2-103">Removes a Management Group</span></span>

## <span data-ttu-id="6d0b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d0b2-104">SYNTAX</span></span>

### <span data-ttu-id="6d0b2-105">GroupOperations (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d0b2-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d0b2-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="6d0b2-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d0b2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d0b2-107">DESCRIPTION</span></span>
<span data-ttu-id="6d0b2-108">O **cmdlet Remove-AzManagementGroup** exclui um Grupo de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="6d0b2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d0b2-109">EXAMPLES</span></span>

### <span data-ttu-id="6d0b2-110">Exemplo 1: Remover um Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d0b2-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="6d0b2-111">Exemplo 2: Remover um Grupo de Gerenciamento por meio de um objeto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d0b2-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="6d0b2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d0b2-112">PARAMETERS</span></span>

### <span data-ttu-id="6d0b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0b2-113">-DefaultProfile</span></span>
<span data-ttu-id="6d0b2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d0b2-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="6d0b2-115">-GroupName</span></span>
<span data-ttu-id="6d0b2-116">ID do Grupo de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6d0b2-116">Management Group Id</span></span>

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

### <span data-ttu-id="6d0b2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d0b2-117">-InputObject</span></span>
<span data-ttu-id="6d0b2-118">Objeto de Entrada da chamada Obter</span><span class="sxs-lookup"><span data-stu-id="6d0b2-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="6d0b2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d0b2-119">-PassThru</span></span>
<span data-ttu-id="6d0b2-120">Retornar `true` após a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="6d0b2-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="6d0b2-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6d0b2-121">-Confirm</span></span>
<span data-ttu-id="6d0b2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d0b2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d0b2-123">-WhatIf</span></span>
<span data-ttu-id="6d0b2-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d0b2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d0b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0b2-126">CommonParameters</span></span>
<span data-ttu-id="6d0b2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d0b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0b2-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d0b2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0b2-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d0b2-129">INPUTS</span></span>

### <span data-ttu-id="6d0b2-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d0b2-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6d0b2-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d0b2-131">OUTPUTS</span></span>

### <span data-ttu-id="6d0b2-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d0b2-132">System.Boolean</span></span>

## <span data-ttu-id="6d0b2-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6d0b2-133">NOTES</span></span>

## <span data-ttu-id="6d0b2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d0b2-134">RELATED LINKS</span></span>
