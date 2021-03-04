---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886270"
---
# <span data-ttu-id="d7632-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="d7632-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="d7632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7632-102">SYNOPSIS</span></span>
<span data-ttu-id="d7632-103">Anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="d7632-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="d7632-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7632-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7632-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7632-105">DESCRIPTION</span></span>
<span data-ttu-id="d7632-106">O cmdlet **Remove-AzApiManagementApiFromGateway** anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="d7632-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="d7632-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7632-107">EXAMPLES</span></span>

### <span data-ttu-id="d7632-108">Exemplo 1: Remover uma API de um gateway</span><span class="sxs-lookup"><span data-stu-id="d7632-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="d7632-109">Este comando remove a API especificada de um gateway.</span><span class="sxs-lookup"><span data-stu-id="d7632-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="d7632-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7632-110">PARAMETERS</span></span>

### <span data-ttu-id="d7632-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7632-111">-ApiId</span></span>
<span data-ttu-id="d7632-112">Identificador de APIs existentes a ser removido do Gateway.</span><span class="sxs-lookup"><span data-stu-id="d7632-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="d7632-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7632-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d7632-114">-Context</span><span class="sxs-lookup"><span data-stu-id="d7632-114">-Context</span></span>
<span data-ttu-id="d7632-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d7632-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7632-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7632-116">This parameter is required.</span></span>

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

### <span data-ttu-id="d7632-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7632-117">-DefaultProfile</span></span>
<span data-ttu-id="d7632-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7632-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7632-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d7632-119">-GatewayId</span></span>
<span data-ttu-id="d7632-120">Identificador do Gateway existente para remover a API.</span><span class="sxs-lookup"><span data-stu-id="d7632-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="d7632-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7632-121">This parameter is required.</span></span>

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

### <span data-ttu-id="d7632-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7632-122">-PassThru</span></span>
<span data-ttu-id="d7632-123">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d7632-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d7632-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7632-124">This parameter is optional.</span></span>
<span data-ttu-id="d7632-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="d7632-125">Default value is false.</span></span>

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

### <span data-ttu-id="d7632-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7632-126">-Confirm</span></span>
<span data-ttu-id="d7632-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7632-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7632-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7632-128">-WhatIf</span></span>
<span data-ttu-id="d7632-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7632-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7632-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7632-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7632-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7632-131">CommonParameters</span></span>
<span data-ttu-id="d7632-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7632-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7632-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7632-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7632-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7632-134">INPUTS</span></span>

### <span data-ttu-id="d7632-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7632-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7632-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d7632-136">System.String</span></span>

### <span data-ttu-id="d7632-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7632-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7632-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7632-138">OUTPUTS</span></span>

### <span data-ttu-id="d7632-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7632-139">System.Boolean</span></span>

## <span data-ttu-id="d7632-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7632-140">NOTES</span></span>

## <span data-ttu-id="d7632-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7632-141">RELATED LINKS</span></span>
