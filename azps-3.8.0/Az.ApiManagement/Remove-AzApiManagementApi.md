---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942197"
---
# <span data-ttu-id="cf198-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="cf198-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf198-102">SYNOPSIS</span></span>
<span data-ttu-id="cf198-103">Remove uma API.</span><span class="sxs-lookup"><span data-stu-id="cf198-103">Removes an API.</span></span>

## <span data-ttu-id="cf198-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf198-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf198-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf198-105">DESCRIPTION</span></span>
<span data-ttu-id="cf198-106">O cmdlet **Remove-AzApiManagementApi** remove uma API existente.</span><span class="sxs-lookup"><span data-stu-id="cf198-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="cf198-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf198-107">EXAMPLES</span></span>

### <span data-ttu-id="cf198-108">Exemplo 1: remover uma API</span><span class="sxs-lookup"><span data-stu-id="cf198-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="cf198-109">Este comando Remove a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="cf198-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="cf198-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf198-110">PARAMETERS</span></span>

### <span data-ttu-id="cf198-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cf198-111">-ApiId</span></span>
<span data-ttu-id="cf198-112">Especifica a ID da API remove.</span><span class="sxs-lookup"><span data-stu-id="cf198-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="cf198-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cf198-113">-Context</span></span>
<span data-ttu-id="cf198-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cf198-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cf198-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf198-115">-DefaultProfile</span></span>
<span data-ttu-id="cf198-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf198-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf198-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf198-117">-PassThru</span></span>
<span data-ttu-id="cf198-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="cf198-118">passthru</span></span>

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

### <span data-ttu-id="cf198-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf198-119">-Confirm</span></span>
<span data-ttu-id="cf198-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf198-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf198-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf198-121">-WhatIf</span></span>
<span data-ttu-id="cf198-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf198-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf198-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf198-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf198-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf198-124">CommonParameters</span></span>
<span data-ttu-id="cf198-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf198-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf198-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf198-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf198-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf198-127">INPUTS</span></span>

### <span data-ttu-id="cf198-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cf198-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cf198-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cf198-129">System.String</span></span>

### <span data-ttu-id="cf198-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cf198-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf198-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf198-131">OUTPUTS</span></span>

### <span data-ttu-id="cf198-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf198-132">System.Boolean</span></span>

## <span data-ttu-id="cf198-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf198-133">NOTES</span></span>

## <span data-ttu-id="cf198-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf198-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf198-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="cf198-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="cf198-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="cf198-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="cf198-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cf198-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


