---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 4ddeee0b0efbb55d98e8e14be1bc84ea83b38e6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886801"
---
# <span data-ttu-id="a6984-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a6984-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="a6984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6984-102">SYNOPSIS</span></span>
<span data-ttu-id="a6984-103">Remove um grupo de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="a6984-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="a6984-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6984-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6984-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6984-105">DESCRIPTION</span></span>
<span data-ttu-id="a6984-106">O cmdlet **Remove-AzApiManagementGroup** remove um grupo de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="a6984-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="a6984-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6984-107">EXAMPLES</span></span>

### <span data-ttu-id="a6984-108">Exemplo 1: Remover um grupo de gerenciamento existente</span><span class="sxs-lookup"><span data-stu-id="a6984-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="a6984-109">Este comando remove um grupo de gerenciamento existente chamado Group0001 e não solicita confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="a6984-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="a6984-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6984-110">PARAMETERS</span></span>

### <span data-ttu-id="a6984-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a6984-111">-Context</span></span>
<span data-ttu-id="a6984-112">Especifica a instância de um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a6984-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6984-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6984-113">-DefaultProfile</span></span>
<span data-ttu-id="a6984-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a6984-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6984-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a6984-115">-GroupId</span></span>
<span data-ttu-id="a6984-116">Especifica o identificador de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="a6984-116">Specifies the identifier of a management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6984-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6984-117">-PassThru</span></span>
<span data-ttu-id="a6984-118">Indica que esse cmdlet retornará um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a6984-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6984-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6984-119">-Confirm</span></span>
<span data-ttu-id="a6984-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6984-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6984-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6984-121">-WhatIf</span></span>
<span data-ttu-id="a6984-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6984-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6984-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6984-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6984-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6984-124">CommonParameters</span></span>
<span data-ttu-id="a6984-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6984-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6984-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6984-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6984-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6984-127">INPUTS</span></span>

### <span data-ttu-id="a6984-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a6984-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a6984-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a6984-129">System.String</span></span>

### <span data-ttu-id="a6984-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6984-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a6984-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6984-131">OUTPUTS</span></span>

### <span data-ttu-id="a6984-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6984-132">System.Boolean</span></span>

## <span data-ttu-id="a6984-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6984-133">NOTES</span></span>

## <span data-ttu-id="a6984-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6984-134">RELATED LINKS</span></span>

[<span data-ttu-id="a6984-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a6984-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="a6984-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a6984-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="a6984-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a6984-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


