---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111229"
---
# <span data-ttu-id="36aa4-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="36aa4-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="36aa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="36aa4-103">Desconecta uma API de um Gateway.</span><span class="sxs-lookup"><span data-stu-id="36aa4-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="36aa4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36aa4-104">SYNTAX</span></span>

### <span data-ttu-id="36aa4-105">ContextParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36aa4-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36aa4-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36aa4-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36aa4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36aa4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36aa4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="36aa4-108">DESCRIPTION</span></span>
<span data-ttu-id="36aa4-109">O cmdlet **Remove-AzApiManagementGateway** desconecta uma API de um Gateway.</span><span class="sxs-lookup"><span data-stu-id="36aa4-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="36aa4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36aa4-110">EXAMPLES</span></span>

### <span data-ttu-id="36aa4-111">Exemplo 1: Remover um gateway existente</span><span class="sxs-lookup"><span data-stu-id="36aa4-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="36aa4-112">Esse comando remove um gateway existente e não solicita confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="36aa4-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="36aa4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36aa4-113">PARAMETERS</span></span>

### <span data-ttu-id="36aa4-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="36aa4-114">-Context</span></span>
<span data-ttu-id="36aa4-115">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="36aa4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="36aa4-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="36aa4-116">This parameter is required.</span></span>

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

### <span data-ttu-id="36aa4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36aa4-117">-DefaultProfile</span></span>
<span data-ttu-id="36aa4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36aa4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36aa4-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="36aa4-119">-GatewayId</span></span>
<span data-ttu-id="36aa4-120">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="36aa4-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="36aa4-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="36aa4-121">This parameter is required.</span></span>

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

### <span data-ttu-id="36aa4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36aa4-122">-InputObject</span></span>
<span data-ttu-id="36aa4-123">Instância do PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="36aa4-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="36aa4-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="36aa4-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36aa4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36aa4-125">-PassThru</span></span>
<span data-ttu-id="36aa4-126">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="36aa4-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="36aa4-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="36aa4-127">This parameter is optional.</span></span>
<span data-ttu-id="36aa4-128">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="36aa4-128">Default value is false.</span></span>

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

### <span data-ttu-id="36aa4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36aa4-129">-ResourceId</span></span>
<span data-ttu-id="36aa4-130">Arm ResourceId do Gateway.</span><span class="sxs-lookup"><span data-stu-id="36aa4-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="36aa4-131">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="36aa4-131">This parameter is required.</span></span>

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

### <span data-ttu-id="36aa4-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="36aa4-132">-Confirm</span></span>
<span data-ttu-id="36aa4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36aa4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36aa4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36aa4-134">-WhatIf</span></span>
<span data-ttu-id="36aa4-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="36aa4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36aa4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36aa4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36aa4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36aa4-137">CommonParameters</span></span>
<span data-ttu-id="36aa4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36aa4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36aa4-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36aa4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36aa4-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="36aa4-140">INPUTS</span></span>

### <span data-ttu-id="36aa4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36aa4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36aa4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="36aa4-142">System.String</span></span>

### <span data-ttu-id="36aa4-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36aa4-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36aa4-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="36aa4-144">OUTPUTS</span></span>

### <span data-ttu-id="36aa4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36aa4-145">System.Boolean</span></span>

## <span data-ttu-id="36aa4-146">Notas</span><span class="sxs-lookup"><span data-stu-id="36aa4-146">NOTES</span></span>

## <span data-ttu-id="36aa4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36aa4-147">RELATED LINKS</span></span>
