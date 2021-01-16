---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272159"
---
# <span data-ttu-id="87da1-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="87da1-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="87da1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87da1-102">SYNOPSIS</span></span>
<span data-ttu-id="87da1-103">Remove uma configuração de nome de host do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="87da1-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="87da1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87da1-104">SYNTAX</span></span>

### <span data-ttu-id="87da1-105">ContextParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="87da1-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87da1-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87da1-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87da1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87da1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87da1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87da1-108">DESCRIPTION</span></span>
<span data-ttu-id="87da1-109">O cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** remove uma configuração de nome de host do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="87da1-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="87da1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87da1-110">EXAMPLES</span></span>

### <span data-ttu-id="87da1-111">Exemplo 1: remover uma configuração de nome de host de gateway existente</span><span class="sxs-lookup"><span data-stu-id="87da1-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="87da1-112">Esse comando Remove uma configuração de nome de host de gateway existente e não solicita confirmação pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="87da1-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="87da1-113">OS</span><span class="sxs-lookup"><span data-stu-id="87da1-113">PARAMETERS</span></span>

### <span data-ttu-id="87da1-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="87da1-114">-Context</span></span>
<span data-ttu-id="87da1-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="87da1-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="87da1-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87da1-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87da1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87da1-117">-DefaultProfile</span></span>
<span data-ttu-id="87da1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87da1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87da1-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="87da1-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="87da1-120">Identificador da configuração de nome do host de gateway existente.</span><span class="sxs-lookup"><span data-stu-id="87da1-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="87da1-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87da1-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da1-122">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="87da1-122">-GatewayId</span></span>
<span data-ttu-id="87da1-123">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="87da1-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="87da1-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87da1-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87da1-125">-InputObject</span></span>
<span data-ttu-id="87da1-126">Instância do PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="87da1-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="87da1-127">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87da1-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87da1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87da1-128">-PassThru</span></span>
<span data-ttu-id="87da1-129">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="87da1-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="87da1-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="87da1-130">This parameter is optional.</span></span>
<span data-ttu-id="87da1-131">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="87da1-131">Default value is false.</span></span>

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

### <span data-ttu-id="87da1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87da1-132">-ResourceId</span></span>
<span data-ttu-id="87da1-133">Resourcebinding do GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="87da1-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="87da1-134">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="87da1-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da1-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87da1-135">-Confirm</span></span>
<span data-ttu-id="87da1-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87da1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87da1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87da1-137">-WhatIf</span></span>
<span data-ttu-id="87da1-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87da1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87da1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87da1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87da1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87da1-140">CommonParameters</span></span>
<span data-ttu-id="87da1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87da1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87da1-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87da1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87da1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87da1-143">INPUTS</span></span>

### <span data-ttu-id="87da1-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87da1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87da1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87da1-145">System.String</span></span>

### <span data-ttu-id="87da1-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87da1-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87da1-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87da1-147">OUTPUTS</span></span>

### <span data-ttu-id="87da1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87da1-148">System.Boolean</span></span>

## <span data-ttu-id="87da1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87da1-149">NOTES</span></span>

## <span data-ttu-id="87da1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87da1-150">RELATED LINKS</span></span>
