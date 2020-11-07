---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954492"
---
# <span data-ttu-id="1290b-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1290b-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="1290b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1290b-102">SYNOPSIS</span></span>
<span data-ttu-id="1290b-103">Desanexa uma API de um gateway.</span><span class="sxs-lookup"><span data-stu-id="1290b-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="1290b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1290b-104">SYNTAX</span></span>

### <span data-ttu-id="1290b-105">ContextParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1290b-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1290b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1290b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1290b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1290b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1290b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1290b-108">DESCRIPTION</span></span>
<span data-ttu-id="1290b-109">O cmdlet **Remove-AzApiManagementGateway** DESANEXA uma API de um gateway.</span><span class="sxs-lookup"><span data-stu-id="1290b-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="1290b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1290b-110">EXAMPLES</span></span>

### <span data-ttu-id="1290b-111">Exemplo 1: remover um gateway existente</span><span class="sxs-lookup"><span data-stu-id="1290b-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="1290b-112">Esse comando Remove um gateway existente e não solicita confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="1290b-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="1290b-113">OS</span><span class="sxs-lookup"><span data-stu-id="1290b-113">PARAMETERS</span></span>

### <span data-ttu-id="1290b-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1290b-114">-Context</span></span>
<span data-ttu-id="1290b-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1290b-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1290b-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1290b-116">This parameter is required.</span></span>

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

### <span data-ttu-id="1290b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1290b-117">-DefaultProfile</span></span>
<span data-ttu-id="1290b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1290b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1290b-119">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="1290b-119">-GatewayId</span></span>
<span data-ttu-id="1290b-120">Identificador do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="1290b-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="1290b-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1290b-121">This parameter is required.</span></span>

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

### <span data-ttu-id="1290b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1290b-122">-InputObject</span></span>
<span data-ttu-id="1290b-123">Instância do PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="1290b-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="1290b-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1290b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="1290b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1290b-125">-PassThru</span></span>
<span data-ttu-id="1290b-126">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1290b-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1290b-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="1290b-127">This parameter is optional.</span></span>
<span data-ttu-id="1290b-128">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="1290b-128">Default value is false.</span></span>

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

### <span data-ttu-id="1290b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1290b-129">-ResourceId</span></span>
<span data-ttu-id="1290b-130">Resourcebinding do gateway.</span><span class="sxs-lookup"><span data-stu-id="1290b-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="1290b-131">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="1290b-131">This parameter is required.</span></span>

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

### <span data-ttu-id="1290b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1290b-132">-Confirm</span></span>
<span data-ttu-id="1290b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1290b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1290b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1290b-134">-WhatIf</span></span>
<span data-ttu-id="1290b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1290b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1290b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1290b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1290b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1290b-137">CommonParameters</span></span>
<span data-ttu-id="1290b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1290b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1290b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1290b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1290b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1290b-140">INPUTS</span></span>

### <span data-ttu-id="1290b-141">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1290b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1290b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1290b-142">System.String</span></span>

### <span data-ttu-id="1290b-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1290b-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1290b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1290b-144">OUTPUTS</span></span>

### <span data-ttu-id="1290b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1290b-145">System.Boolean</span></span>

## <span data-ttu-id="1290b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1290b-146">NOTES</span></span>

## <span data-ttu-id="1290b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1290b-147">RELATED LINKS</span></span>
