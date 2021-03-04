---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886114"
---
# <span data-ttu-id="c4a4e-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="c4a4e-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="c4a4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a4e-103">Remove um valor nomeado de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="c4a4e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4a4e-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a4e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4a4e-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a4e-106">O cmdlet **Remove-AzApiManagementNamedValue** remove um gerenciamento de API do Azure **chamado Valor**.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="c4a4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a4e-108">Exemplo 1: Remover o valor nomeado</span><span class="sxs-lookup"><span data-stu-id="c4a4e-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="c4a4e-109">Este comando remove o valor nomeado que tem a propriedade ID11.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="c4a4e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-110">PARAMETERS</span></span>

### <span data-ttu-id="c4a4e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c4a4e-111">-Context</span></span>
<span data-ttu-id="c4a4e-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c4a4e-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c4a4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a4e-114">-DefaultProfile</span></span>
<span data-ttu-id="c4a4e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a4e-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="c4a4e-116">-NamedValueId</span></span>
<span data-ttu-id="c4a4e-117">Identificador do valor nomeado existente.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-117">Identifier of existing named value.</span></span>
<span data-ttu-id="c4a4e-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c4a4e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4a4e-119">-PassThru</span></span>
<span data-ttu-id="c4a4e-120">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c4a4e-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-121">This parameter is optional.</span></span>
<span data-ttu-id="c4a4e-122">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-122">Default value is false.</span></span>

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

### <span data-ttu-id="c4a4e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a4e-123">-Confirm</span></span>
<span data-ttu-id="c4a4e-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a4e-125">-WhatIf</span></span>
<span data-ttu-id="c4a4e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a4e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a4e-128">CommonParameters</span></span>
<span data-ttu-id="c4a4e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a4e-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a4e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-131">INPUTS</span></span>

### <span data-ttu-id="c4a4e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4a4e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4a4e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4a4e-133">System.String</span></span>

### <span data-ttu-id="c4a4e-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4a4e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4a4e-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-135">OUTPUTS</span></span>

### <span data-ttu-id="c4a4e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4a4e-136">System.Boolean</span></span>

## <span data-ttu-id="c4a4e-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4a4e-137">NOTES</span></span>

## <span data-ttu-id="c4a4e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4a4e-138">RELATED LINKS</span></span>
