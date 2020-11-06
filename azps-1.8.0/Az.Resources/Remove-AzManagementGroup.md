---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: cbc6be671669b3db8af41c0e5de4333b811e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599344"
---
# <span data-ttu-id="d034f-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d034f-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="d034f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d034f-102">SYNOPSIS</span></span>
<span data-ttu-id="d034f-103">Remove um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d034f-103">Removes a Management Group</span></span>

## <span data-ttu-id="d034f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d034f-104">SYNTAX</span></span>

### <span data-ttu-id="d034f-105">GroupOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="d034f-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d034f-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="d034f-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d034f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d034f-107">DESCRIPTION</span></span>
<span data-ttu-id="d034f-108">O cmdlet **Remove-AzManagementGroup** exclui um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d034f-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="d034f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d034f-109">EXAMPLES</span></span>

### <span data-ttu-id="d034f-110">Exemplo 1-remover um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d034f-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="d034f-111">Exemplo 2-Remova um grupo de gerenciamento por objeto de PSManagementGroup de tubulação</span><span class="sxs-lookup"><span data-stu-id="d034f-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="d034f-112">OS</span><span class="sxs-lookup"><span data-stu-id="d034f-112">PARAMETERS</span></span>

### <span data-ttu-id="d034f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d034f-113">-DefaultProfile</span></span>
<span data-ttu-id="d034f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d034f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d034f-115">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="d034f-115">-GroupName</span></span>
<span data-ttu-id="d034f-116">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d034f-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d034f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d034f-117">-InputObject</span></span>
<span data-ttu-id="d034f-118">Objeto de entrada da chamada Get</span><span class="sxs-lookup"><span data-stu-id="d034f-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="d034f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d034f-119">-PassThru</span></span>
<span data-ttu-id="d034f-120">Retorno `true` sobre a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="d034f-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="d034f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d034f-121">-Confirm</span></span>
<span data-ttu-id="d034f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d034f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d034f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d034f-123">-WhatIf</span></span>
<span data-ttu-id="d034f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d034f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d034f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d034f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d034f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d034f-126">CommonParameters</span></span>
<span data-ttu-id="d034f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d034f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d034f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d034f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d034f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d034f-129">INPUTS</span></span>

### <span data-ttu-id="d034f-130">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d034f-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="d034f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d034f-131">OUTPUTS</span></span>

### <span data-ttu-id="d034f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d034f-132">System.Boolean</span></span>

## <span data-ttu-id="d034f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d034f-133">NOTES</span></span>

## <span data-ttu-id="d034f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d034f-134">RELATED LINKS</span></span>
