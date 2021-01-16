---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262393"
---
# <span data-ttu-id="cd579-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="cd579-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="cd579-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd579-102">SYNOPSIS</span></span>
<span data-ttu-id="cd579-103">Anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="cd579-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="cd579-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd579-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd579-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd579-105">DESCRIPTION</span></span>
<span data-ttu-id="cd579-106">O cmdlet **Remove-AzApiManagementApiFromGateway** anexa uma API a um gateway.</span><span class="sxs-lookup"><span data-stu-id="cd579-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="cd579-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd579-107">EXAMPLES</span></span>

### <span data-ttu-id="cd579-108">Exemplo 1: remover uma API de um gateway</span><span class="sxs-lookup"><span data-stu-id="cd579-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="cd579-109">Esse comando Remove a API especificada de um gateway.</span><span class="sxs-lookup"><span data-stu-id="cd579-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="cd579-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd579-110">PARAMETERS</span></span>

### <span data-ttu-id="cd579-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cd579-111">-ApiId</span></span>
<span data-ttu-id="cd579-112">Identificador de APIs existentes para remover do gateway.</span><span class="sxs-lookup"><span data-stu-id="cd579-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="cd579-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd579-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cd579-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cd579-114">-Context</span></span>
<span data-ttu-id="cd579-115">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cd579-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cd579-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd579-116">This parameter is required.</span></span>

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

### <span data-ttu-id="cd579-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd579-117">-DefaultProfile</span></span>
<span data-ttu-id="cd579-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd579-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd579-119">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="cd579-119">-GatewayId</span></span>
<span data-ttu-id="cd579-120">Identificador do gateway existente do qual remover a API.</span><span class="sxs-lookup"><span data-stu-id="cd579-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="cd579-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cd579-121">This parameter is required.</span></span>

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

### <span data-ttu-id="cd579-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd579-122">-PassThru</span></span>
<span data-ttu-id="cd579-123">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cd579-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="cd579-124">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="cd579-124">This parameter is optional.</span></span>
<span data-ttu-id="cd579-125">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="cd579-125">Default value is false.</span></span>

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

### <span data-ttu-id="cd579-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd579-126">-Confirm</span></span>
<span data-ttu-id="cd579-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd579-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd579-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd579-128">-WhatIf</span></span>
<span data-ttu-id="cd579-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd579-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd579-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd579-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd579-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd579-131">CommonParameters</span></span>
<span data-ttu-id="cd579-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd579-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd579-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd579-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd579-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd579-134">INPUTS</span></span>

### <span data-ttu-id="cd579-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd579-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd579-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cd579-136">System.String</span></span>

### <span data-ttu-id="cd579-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cd579-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd579-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd579-138">OUTPUTS</span></span>

### <span data-ttu-id="cd579-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd579-139">System.Boolean</span></span>

## <span data-ttu-id="cd579-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd579-140">NOTES</span></span>

## <span data-ttu-id="cd579-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd579-141">RELATED LINKS</span></span>
