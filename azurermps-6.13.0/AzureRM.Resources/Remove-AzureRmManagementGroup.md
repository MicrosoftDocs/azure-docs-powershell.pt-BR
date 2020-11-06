---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433187"
---
# <span data-ttu-id="fecfd-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fecfd-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="fecfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fecfd-102">SYNOPSIS</span></span>
<span data-ttu-id="fecfd-103">Remove um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fecfd-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fecfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fecfd-104">SYNTAX</span></span>

### <span data-ttu-id="fecfd-105">GroupOperations (padrão)</span><span class="sxs-lookup"><span data-stu-id="fecfd-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecfd-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="fecfd-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fecfd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fecfd-107">DESCRIPTION</span></span>
<span data-ttu-id="fecfd-108">O cmdlet **Remove-AzureRmManagementGroup** exclui um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fecfd-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="fecfd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fecfd-109">EXAMPLES</span></span>

### <span data-ttu-id="fecfd-110">Exemplo 1-remover um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fecfd-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="fecfd-111">Exemplo 2-Remova um grupo de gerenciamento por objeto de PSManagementGroup de tubulação</span><span class="sxs-lookup"><span data-stu-id="fecfd-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="fecfd-112">OS</span><span class="sxs-lookup"><span data-stu-id="fecfd-112">PARAMETERS</span></span>

### <span data-ttu-id="fecfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecfd-113">-DefaultProfile</span></span>
<span data-ttu-id="fecfd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fecfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fecfd-115">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="fecfd-115">-GroupName</span></span>
<span data-ttu-id="fecfd-116">ID do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fecfd-116">Management Group Id</span></span>

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

### <span data-ttu-id="fecfd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fecfd-117">-InputObject</span></span>
<span data-ttu-id="fecfd-118">Objeto de entrada da chamada Get</span><span class="sxs-lookup"><span data-stu-id="fecfd-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="fecfd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fecfd-119">-PassThru</span></span>
<span data-ttu-id="fecfd-120">Retorno `true` sobre a execução bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="fecfd-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="fecfd-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fecfd-121">-Confirm</span></span>
<span data-ttu-id="fecfd-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fecfd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecfd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecfd-123">-WhatIf</span></span>
<span data-ttu-id="fecfd-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fecfd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fecfd-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fecfd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fecfd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecfd-126">CommonParameters</span></span>
<span data-ttu-id="fecfd-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecfd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecfd-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fecfd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecfd-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fecfd-129">INPUTS</span></span>

### <span data-ttu-id="fecfd-130">Microsoft. Azure. Commands. Resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fecfd-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="fecfd-131">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fecfd-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fecfd-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fecfd-132">OUTPUTS</span></span>

### <span data-ttu-id="fecfd-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fecfd-133">System.Boolean</span></span>

## <span data-ttu-id="fecfd-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fecfd-134">NOTES</span></span>

## <span data-ttu-id="fecfd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fecfd-135">RELATED LINKS</span></span>
