---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432768"
---
# <span data-ttu-id="c6009-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="c6009-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="c6009-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6009-102">SYNOPSIS</span></span>
<span data-ttu-id="c6009-103">Anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="c6009-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="c6009-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6009-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6009-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6009-105">DESCRIPTION</span></span>
<span data-ttu-id="c6009-106">O cmdlet **Add-AzApiManagementApiToGateway** adiciona uma API de gerenciamento de API do Azure a um gateway.</span><span class="sxs-lookup"><span data-stu-id="c6009-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="c6009-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6009-107">EXAMPLES</span></span>

### <span data-ttu-id="c6009-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6009-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="c6009-109">Esse comando adiciona a API especificada ao gateway especificado.</span><span class="sxs-lookup"><span data-stu-id="c6009-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="c6009-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6009-110">PARAMETERS</span></span>

### <span data-ttu-id="c6009-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c6009-111">-ApiId</span></span>
<span data-ttu-id="c6009-112">Identificador de API existente.</span><span class="sxs-lookup"><span data-stu-id="c6009-112">Identifier of existing API.</span></span>
<span data-ttu-id="c6009-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c6009-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c6009-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c6009-114">-Context</span></span>
<span data-ttu-id="c6009-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c6009-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6009-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c6009-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c6009-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6009-117">-DefaultProfile</span></span>
<span data-ttu-id="c6009-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6009-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6009-119">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="c6009-119">-GatewayId</span></span>
<span data-ttu-id="c6009-120">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="c6009-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="c6009-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c6009-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c6009-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6009-122">-PassThru</span></span>
<span data-ttu-id="c6009-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c6009-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c6009-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c6009-124">This parameter is optional.</span></span>
<span data-ttu-id="c6009-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="c6009-125">Default value is false.</span></span>

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

### <span data-ttu-id="c6009-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="c6009-126">-ProvisioningState</span></span>
<span data-ttu-id="c6009-127">Estado de provisionamento (criado).</span><span class="sxs-lookup"><span data-stu-id="c6009-127">Provisioning State (Created).</span></span>
<span data-ttu-id="c6009-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c6009-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="c6009-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6009-129">-Confirm</span></span>
<span data-ttu-id="c6009-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6009-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6009-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6009-131">-WhatIf</span></span>
<span data-ttu-id="c6009-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6009-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6009-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6009-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6009-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6009-134">CommonParameters</span></span>
<span data-ttu-id="c6009-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6009-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6009-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6009-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6009-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6009-137">INPUTS</span></span>

### <span data-ttu-id="c6009-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6009-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6009-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6009-139">System.String</span></span>

### <span data-ttu-id="c6009-140">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c6009-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c6009-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c6009-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c6009-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6009-142">OUTPUTS</span></span>

### <span data-ttu-id="c6009-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6009-143">System.Boolean</span></span>

## <span data-ttu-id="c6009-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6009-144">NOTES</span></span>

## <span data-ttu-id="c6009-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6009-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6009-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="c6009-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)