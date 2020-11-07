---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: df342b3ec96f8bfa8ba882bac2ae620456286012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771395"
---
# <span data-ttu-id="b6a07-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="b6a07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6a07-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a07-103">Remove uma API.</span><span class="sxs-lookup"><span data-stu-id="b6a07-103">Removes an API.</span></span>

## <span data-ttu-id="b6a07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6a07-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6a07-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a07-106">O cmdlet **Remove-AzApiManagementApi** remove uma API existente.</span><span class="sxs-lookup"><span data-stu-id="b6a07-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="b6a07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6a07-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a07-108">Exemplo 1: remover uma API</span><span class="sxs-lookup"><span data-stu-id="b6a07-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="b6a07-109">Este comando Remove a API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="b6a07-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="b6a07-110">OS</span><span class="sxs-lookup"><span data-stu-id="b6a07-110">PARAMETERS</span></span>

### <span data-ttu-id="b6a07-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b6a07-111">-ApiId</span></span>
<span data-ttu-id="b6a07-112">Especifica a ID da API remove.</span><span class="sxs-lookup"><span data-stu-id="b6a07-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="b6a07-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b6a07-113">-Context</span></span>
<span data-ttu-id="b6a07-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b6a07-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a07-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a07-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a07-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a07-117">-PassThru</span></span>
<span data-ttu-id="b6a07-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a07-118">passthru</span></span>

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

### <span data-ttu-id="b6a07-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6a07-119">-Confirm</span></span>
<span data-ttu-id="b6a07-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a07-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a07-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a07-121">-WhatIf</span></span>
<span data-ttu-id="b6a07-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6a07-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a07-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6a07-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a07-124">CommonParameters</span></span>
<span data-ttu-id="b6a07-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a07-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a07-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a07-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6a07-127">INPUTS</span></span>

### <span data-ttu-id="b6a07-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6a07-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b6a07-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a07-129">System.String</span></span>

### <span data-ttu-id="b6a07-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6a07-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6a07-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6a07-131">OUTPUTS</span></span>

### <span data-ttu-id="b6a07-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6a07-132">System.Boolean</span></span>

## <span data-ttu-id="b6a07-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6a07-133">NOTES</span></span>

## <span data-ttu-id="b6a07-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6a07-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6a07-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="b6a07-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="b6a07-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="b6a07-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="b6a07-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b6a07-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


