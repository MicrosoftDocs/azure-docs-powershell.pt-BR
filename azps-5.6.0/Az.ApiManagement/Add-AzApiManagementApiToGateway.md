---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 9c6d556845192a4bd6e5d6c856d113be4a4074a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888013"
---
# <span data-ttu-id="3d315-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="3d315-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="3d315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d315-102">SYNOPSIS</span></span>
<span data-ttu-id="3d315-103">Anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="3d315-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="3d315-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d315-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d315-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d315-105">DESCRIPTION</span></span>
<span data-ttu-id="3d315-106">O cmdlet **Add-AzApiManagementApiToGateway** adiciona uma API de Gerenciamento de API do Azure a um Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d315-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="3d315-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d315-107">EXAMPLES</span></span>

### <span data-ttu-id="3d315-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d315-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="3d315-109">Este comando adiciona a API especificada ao Gateway especificado.</span><span class="sxs-lookup"><span data-stu-id="3d315-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="3d315-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d315-110">PARAMETERS</span></span>

### <span data-ttu-id="3d315-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3d315-111">-ApiId</span></span>
<span data-ttu-id="3d315-112">Identificador da API existente.</span><span class="sxs-lookup"><span data-stu-id="3d315-112">Identifier of existing API.</span></span>
<span data-ttu-id="3d315-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3d315-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3d315-114">-Context</span><span class="sxs-lookup"><span data-stu-id="3d315-114">-Context</span></span>
<span data-ttu-id="3d315-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3d315-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3d315-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3d315-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3d315-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d315-117">-DefaultProfile</span></span>
<span data-ttu-id="3d315-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d315-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d315-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3d315-119">-GatewayId</span></span>
<span data-ttu-id="3d315-120">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="3d315-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="3d315-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3d315-121">This parameter is required.</span></span>

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

### <span data-ttu-id="3d315-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d315-122">-PassThru</span></span>
<span data-ttu-id="3d315-123">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3d315-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3d315-124">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3d315-124">This parameter is optional.</span></span>
<span data-ttu-id="3d315-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="3d315-125">Default value is false.</span></span>

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

### <span data-ttu-id="3d315-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="3d315-126">-ProvisioningState</span></span>
<span data-ttu-id="3d315-127">Estado de provisionamento (Criado).</span><span class="sxs-lookup"><span data-stu-id="3d315-127">Provisioning State (Created).</span></span>
<span data-ttu-id="3d315-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3d315-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d315-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d315-129">-Confirm</span></span>
<span data-ttu-id="3d315-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d315-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d315-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d315-131">-WhatIf</span></span>
<span data-ttu-id="3d315-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d315-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d315-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d315-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d315-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d315-134">CommonParameters</span></span>
<span data-ttu-id="3d315-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d315-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d315-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d315-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d315-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d315-137">INPUTS</span></span>

### <span data-ttu-id="3d315-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d315-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d315-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3d315-139">System.String</span></span>

### <span data-ttu-id="3d315-140">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3d315-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3d315-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d315-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d315-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d315-142">OUTPUTS</span></span>

### <span data-ttu-id="3d315-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d315-143">System.Boolean</span></span>

## <span data-ttu-id="3d315-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d315-144">NOTES</span></span>

## <span data-ttu-id="3d315-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d315-145">RELATED LINKS</span></span>

[<span data-ttu-id="3d315-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="3d315-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)