---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284344"
---
# <span data-ttu-id="1ce55-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1ce55-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="1ce55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ce55-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce55-103">Configura um gateway de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ce55-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="1ce55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ce55-104">SYNTAX</span></span>

### <span data-ttu-id="1ce55-105">ExpandedParameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ce55-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce55-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ce55-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ce55-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ce55-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce55-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ce55-108">DESCRIPTION</span></span>
<span data-ttu-id="1ce55-109">O cmdlet **Update-AzApiManagementGateway** configura um gateway de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1ce55-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="1ce55-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ce55-110">EXAMPLES</span></span>

### <span data-ttu-id="1ce55-111">Exemplo 1: configurar um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="1ce55-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="1ce55-112">Esse comando configura um gateway.</span><span class="sxs-lookup"><span data-stu-id="1ce55-112">This command configures a gateway.</span></span>

## <span data-ttu-id="1ce55-113">OS</span><span class="sxs-lookup"><span data-stu-id="1ce55-113">PARAMETERS</span></span>

### <span data-ttu-id="1ce55-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1ce55-114">-Context</span></span>
<span data-ttu-id="1ce55-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1ce55-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1ce55-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1ce55-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce55-117">-DefaultProfile</span></span>
<span data-ttu-id="1ce55-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ce55-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ce55-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1ce55-119">-Description</span></span>
<span data-ttu-id="1ce55-120">Descrição do gateway.</span><span class="sxs-lookup"><span data-stu-id="1ce55-120">Gateway description.</span></span>
<span data-ttu-id="1ce55-121">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1ce55-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-122">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="1ce55-122">-GatewayId</span></span>
<span data-ttu-id="1ce55-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="1ce55-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="1ce55-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1ce55-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce55-125">-InputObject</span></span>
<span data-ttu-id="1ce55-126">Instância do PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="1ce55-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="1ce55-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1ce55-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="1ce55-128">-LocationData</span></span>
<span data-ttu-id="1ce55-129">Localização do gateway.</span><span class="sxs-lookup"><span data-stu-id="1ce55-129">Gateway location.</span></span>
<span data-ttu-id="1ce55-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1ce55-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ce55-131">-PassThru</span></span>
<span data-ttu-id="1ce55-132">Se especificado, a instância do tipo Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGateway que representa o gateway modificado.</span><span class="sxs-lookup"><span data-stu-id="1ce55-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="1ce55-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ce55-133">-ResourceId</span></span>
<span data-ttu-id="1ce55-134">Resourcebinding do gateway.</span><span class="sxs-lookup"><span data-stu-id="1ce55-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="1ce55-135">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1ce55-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ce55-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ce55-136">-Confirm</span></span>
<span data-ttu-id="1ce55-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ce55-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce55-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce55-138">-WhatIf</span></span>
<span data-ttu-id="1ce55-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ce55-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce55-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ce55-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce55-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce55-141">CommonParameters</span></span>
<span data-ttu-id="1ce55-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce55-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce55-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ce55-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce55-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ce55-144">INPUTS</span></span>

### <span data-ttu-id="1ce55-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1ce55-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ce55-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1ce55-146">System.String</span></span>

### <span data-ttu-id="1ce55-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="1ce55-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="1ce55-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ce55-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ce55-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ce55-149">OUTPUTS</span></span>

### <span data-ttu-id="1ce55-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1ce55-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="1ce55-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ce55-151">NOTES</span></span>

## <span data-ttu-id="1ce55-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ce55-152">RELATED LINKS</span></span>
