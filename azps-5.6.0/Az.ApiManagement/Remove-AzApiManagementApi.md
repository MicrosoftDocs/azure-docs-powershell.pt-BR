---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: d1ef516fc8b95814685350eb309e0a56d08d4b59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886275"
---
# <span data-ttu-id="ccf03-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="ccf03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf03-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf03-103">Remove uma API.</span><span class="sxs-lookup"><span data-stu-id="ccf03-103">Removes an API.</span></span>

## <span data-ttu-id="ccf03-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ccf03-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf03-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ccf03-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf03-106">O cmdlet **Remove-AzApiManagementApi** remove uma API existente.</span><span class="sxs-lookup"><span data-stu-id="ccf03-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="ccf03-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccf03-107">EXAMPLES</span></span>

### <span data-ttu-id="ccf03-108">Exemplo 1: Remover uma API</span><span class="sxs-lookup"><span data-stu-id="ccf03-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="ccf03-109">Este comando remove a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ccf03-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="ccf03-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ccf03-110">PARAMETERS</span></span>

### <span data-ttu-id="ccf03-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ccf03-111">-ApiId</span></span>
<span data-ttu-id="ccf03-112">Especifica a ID da removeção da API.</span><span class="sxs-lookup"><span data-stu-id="ccf03-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="ccf03-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ccf03-113">-Context</span></span>
<span data-ttu-id="ccf03-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="ccf03-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ccf03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf03-115">-DefaultProfile</span></span>
<span data-ttu-id="ccf03-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ccf03-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccf03-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf03-117">-PassThru</span></span>
<span data-ttu-id="ccf03-118">passthru</span><span class="sxs-lookup"><span data-stu-id="ccf03-118">passthru</span></span>

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

### <span data-ttu-id="ccf03-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccf03-119">-Confirm</span></span>
<span data-ttu-id="ccf03-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccf03-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf03-121">-WhatIf</span></span>
<span data-ttu-id="ccf03-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ccf03-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf03-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ccf03-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf03-124">CommonParameters</span></span>
<span data-ttu-id="ccf03-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf03-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccf03-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf03-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccf03-127">INPUTS</span></span>

### <span data-ttu-id="ccf03-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ccf03-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ccf03-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ccf03-129">System.String</span></span>

### <span data-ttu-id="ccf03-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ccf03-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ccf03-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ccf03-131">OUTPUTS</span></span>

### <span data-ttu-id="ccf03-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ccf03-132">System.Boolean</span></span>

## <span data-ttu-id="ccf03-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ccf03-133">NOTES</span></span>

## <span data-ttu-id="ccf03-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccf03-134">RELATED LINKS</span></span>

[<span data-ttu-id="ccf03-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="ccf03-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="ccf03-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="ccf03-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="ccf03-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ccf03-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


