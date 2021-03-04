---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 9a5c4d553f425d7922fa927451ca9f3029a9f4b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888009"
---
# <span data-ttu-id="db6ca-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db6ca-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="db6ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="db6ca-103">Remove um Backend.</span><span class="sxs-lookup"><span data-stu-id="db6ca-103">Removes a Backend.</span></span>

## <span data-ttu-id="db6ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db6ca-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6ca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db6ca-105">DESCRIPTION</span></span>
<span data-ttu-id="db6ca-106">Remove um back-end especificado pelo Identificador do Gerenciamento de Api.</span><span class="sxs-lookup"><span data-stu-id="db6ca-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="db6ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db6ca-107">EXAMPLES</span></span>

### <span data-ttu-id="db6ca-108">Exemplo 1: Remover o Back-end 123</span><span class="sxs-lookup"><span data-stu-id="db6ca-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="db6ca-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db6ca-109">PARAMETERS</span></span>

### <span data-ttu-id="db6ca-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="db6ca-110">-BackendId</span></span>
<span data-ttu-id="db6ca-111">Identificador de back-end existente.</span><span class="sxs-lookup"><span data-stu-id="db6ca-111">Identifier of existing backend.</span></span>
<span data-ttu-id="db6ca-112">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="db6ca-112">This parameter is required.</span></span>

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

### <span data-ttu-id="db6ca-113">-Context</span><span class="sxs-lookup"><span data-stu-id="db6ca-113">-Context</span></span>
<span data-ttu-id="db6ca-114">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="db6ca-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db6ca-115">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="db6ca-115">This parameter is required.</span></span>

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

### <span data-ttu-id="db6ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6ca-116">-DefaultProfile</span></span>
<span data-ttu-id="db6ca-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="db6ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6ca-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6ca-118">-PassThru</span></span>
<span data-ttu-id="db6ca-119">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db6ca-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="db6ca-120">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="db6ca-120">This parameter is optional.</span></span>
<span data-ttu-id="db6ca-121">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="db6ca-121">Default value is false.</span></span>

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

### <span data-ttu-id="db6ca-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db6ca-122">-Confirm</span></span>
<span data-ttu-id="db6ca-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6ca-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6ca-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6ca-124">-WhatIf</span></span>
<span data-ttu-id="db6ca-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db6ca-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db6ca-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db6ca-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6ca-127">CommonParameters</span></span>
<span data-ttu-id="db6ca-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6ca-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db6ca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6ca-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db6ca-130">INPUTS</span></span>

### <span data-ttu-id="db6ca-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db6ca-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db6ca-132">System.String</span><span class="sxs-lookup"><span data-stu-id="db6ca-132">System.String</span></span>

### <span data-ttu-id="db6ca-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db6ca-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db6ca-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db6ca-134">OUTPUTS</span></span>

### <span data-ttu-id="db6ca-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db6ca-135">System.Boolean</span></span>

## <span data-ttu-id="db6ca-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="db6ca-136">NOTES</span></span>

## <span data-ttu-id="db6ca-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db6ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="db6ca-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db6ca-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="db6ca-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db6ca-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="db6ca-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="db6ca-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="db6ca-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="db6ca-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="db6ca-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db6ca-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
